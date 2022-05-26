```
pub contract CryptoPoops {
  pub var totalSupply: UInt64

  // This is an NFT resource that contains a name,
  // favouriteFood, and luckyNumber
  pub resource NFT {
    pub let id: UInt64

    pub let name: String
    pub let favouriteFood: String
    pub let luckyNumber: Int

    init(_name: String, _favouriteFood: String, _luckyNumber: Int) {
      self.id = self.uuid

      self.name = _name
      self.favouriteFood = _favouriteFood
      self.luckyNumber = _luckyNumber
    }
  }

  // This is the resource interface for the CollectionPublic resource: 
  // This inteface exposes the deposit, getIDS and borrowNFT functions:
  // (so we can access them publicly via a script or transaction)
  pub resource interface CollectionPublic {
    pub fun deposit(token: @NFT)
    pub fun getIDs(): [UInt64]
    pub fun borrowNFT(id: UInt64): &NFT
  }

  // The actual resource for CollectionPublic
  pub resource Collection: CollectionPublic {
    pub var ownedNFTs: @{UInt64: NFT}

  // A resource-scoped function which allows us to deposit an NFT into the collection.
    pub fun deposit(token: @NFT) {
      self.ownedNFTs[token.id] <-! token
    }

  // A resource-scoped function which allows us to withdraw an NFT from the collection using the "remove" method.
    pub fun withdraw(withdrawID: UInt64): @NFT {
      let nft <- self.ownedNFTs.remove(key: withdrawID) 
              ?? panic("This NFT does not exist in this Collection.")
      return <- nft
    }
  
  // A resource-scoped function which allows us to gain all the id from our NFTs using the "keys" method
    pub fun getIDs(): [UInt64] {
      return self.ownedNFTs.keys
    }
    
    // A resource-scoped borrow function which returns a reference so we can read the NFT later from a script. 
    pub fun borrowNFT(id: UInt64): &NFT {
      return &self.ownedNFTs[id] as &NFT
    }

    init() {
      self.ownedNFTs <- {}
    }

    destroy() {
      destroy self.ownedNFTs
    }
  }

  // Function to create an empty collection.
  pub fun createEmptyCollection(): @Collection {
    return <- create Collection()
  }

  // We define a new Minter resource here
  // Using init we ensure that only the account belonging to the deployer of the contract will have access to this.
  pub resource Minter {
  
  // Function within Minter resource which creates the NFT using the attributes defined above.
    pub fun createNFT(name: String, favouriteFood: String, luckyNumber: Int): @NFT {
      return <- create NFT(_name: name, _favouriteFood: favouriteFood, _luckyNumber: luckyNumber)
    }
  
  // Function to create the Minter resource.
    pub fun createMinter(): @Minter {
      return <- create Minter()
    }

  }

  init() {
    self.totalSupply = 0
    self.account.save(<- create Minter(), to: /storage/Minter)
  }
}

```
