**1. What does "force casting" with as! do? Why is it useful in our Collection?**

The `as!` syntax "downcasts" the generic NFT type from the official Flow NFT standard to our specific NFT from our collection. This is useful because the generic type only has an id field and potentially we want to add a lot more  fields which could be specific to our unique NFT project.

**2. What does auth do? When do we use it?**

Auth is a special keyword (standing for authorise) which we must use when downcasting a reference. In this case we are downcasting a reference to the `NonFungibleToken.NFT` to enable the specific use of our custom `NFT`.

**3. This last quest will be your most difficult yet.**

(`borrowAuthNFT` function added to implementating contract):

i.) Set up accounts:

The transaction below sets up an account, creates an empty collection and creates a public link to make the collection viewable to the public:

<img width="1217" alt="Screenshot 2022-05-31 at 11 23 48" src="https://user-images.githubusercontent.com/4712052/171152556-7a60ce75-aff5-4004-a708-a2f247a79555.png">

ii.) Mint the NFT:

<img width="977" alt="Screenshot 2022-05-31 at 11 24 54" src="https://user-images.githubusercontent.com/4712052/171153788-bf9f2089-73c8-440b-9269-8091bd9fc90e.png">

The output produces this log (and no errors):

<img width="595" alt="Screenshot 2022-05-31 at 10 47 21" src="https://user-images.githubusercontent.com/4712052/171145524-6fa48413-a521-4f19-bfdb-c590c1cbc473.png">

iii.) Script to read the NFT metadata:

I can log all the metadata in one go from the whole NFT resource by specifying the return type to be `&NonFungibleToken.NFT` as shown in script below:

<img width="774" alt="Screenshot 2022-05-31 at 11 32 56" src="https://user-images.githubusercontent.com/4712052/171154236-cbfa5e00-11b0-482f-90cd-3f23052693d8.png">

I then get this full output when selecting a certain id:

`{"type":"Optional","value":{"type":"Resource","value":{"id":"A.0000000000000002.CryptoPoops.NFT","fields":[{"name":"uuid","value":{"type":"UInt64","value":"2"}},{"name":"id","value":{"type":"UInt64","value":"2"}},{"name":"name","value":{"type":"String","value":"PoopyMcPoopyson"}},{"name":"favouriteFood","value":{"type":"String","value":"Pizza"}},{"name":"luckyNumber","value":{"type":"Int","value":"8"}}]}}}`

The output above is not super-readable so I can also select specific metadata "attributes" such as favourite food as shown in the modified Script below (while also changing the return type to be a String):

<img width="768" alt="Screenshot 2022-05-31 at 11 35 41" src="https://user-images.githubusercontent.com/4712052/171154631-ce7477af-68e8-4419-a382-ce49b13a1d9b.png">

Output for ID 2:

<img width="526" alt="Screenshot 2022-05-31 at 11 36 14" src="https://user-images.githubusercontent.com/4712052/171154696-bbacfb98-00a5-4c97-ba26-d7ca56817a61.png">

Output for ID 5:

<img width="565" alt="Screenshot 2022-05-31 at 11 36 51" src="https://user-images.githubusercontent.com/4712052/171154781-86abfd38-8f4e-438a-b9f7-7d0c835955af.png">









