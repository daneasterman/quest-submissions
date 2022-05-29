**1. What does "force casting" with as! do? Why is it useful in our Collection?**

The `as!` syntax "downcasts" the generic NFT type from the official Flow NFT standard to our specific NFT from our collection. This is useful because the generic type only has an id field and potentially we want to add a lot more  fields which could be specific to our unique NFT project.

**2. What does auth do? When do we use it?**

Auth is a special keyword (standing for authorise) which we must use when downcasting a reference. In this case we are downcasting a reference to the `NonFungibleToken.NFT` to enable the specific use of our custom `NFT`.

**3. This last quest will be your most difficult yet.**

<!-- CONTRACT TO DO -->
i.) Add `borrowAuthNFT` function - as in example.

<!-- Transactions TO DO: -->
i.) Set up accounts.
ii.) Mint the NFT.
iii.) Script to read the NFT metadata.
