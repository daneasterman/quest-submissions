**1. What does .link() do?**

Link creates a "capability" which acts as a pointer from the `/storage/` path to the `/public/` or `/private` path so other people can read/view our resource. In practice, the private path is not used very often in Cadence / Flow.

**2. In your own words (no code), explain how we can use resource interfaces to only expose certain things to the /public/ path.**

By using an interface we can have more granular control over which data or functions are accessible via the `/public/` path from a script. As mentioned in the example, we might want an NFT's name to be publicly accessible but definitely not a function which would allow anyone to arbitrarily change the name of that NFT.

**3. Deploy a contract that contains a resource that implements a resource interface. Then, do the following:**

<img width="373" alt="Screenshot 2022-05-18 at 17 12 31" src="https://user-images.githubusercontent.com/4712052/169091038-265d21cc-a0e1-46c7-afaa-b0bc0229cbe9.png">

**i.) In a transaction, save the resource to storage and link it to the public with the restrictive interface.**

<img width="807" alt="Screenshot 2022-05-18 at 17 13 36" src="https://user-images.githubusercontent.com/4712052/169091250-016c00e2-b384-4b1f-ab4b-28b6739b2e77.png">

**ii.) Run a script that tries to access a non-exposed field in the resource interface, and see the error pop up.**

Here I have not exposed the `catMintCount` variable in the interface of my Smart Contract so I get an error:

<img width="830" alt="Screenshot 2022-05-18 at 17 28 37" src="https://user-images.githubusercontent.com/4712052/169094239-9547a298-b4e0-4c49-bd81-4ce590d91852.png">


**iii.) Run the script and access something you CAN read from. Return it from the script.**

But I have allowed `catName` to be accessible:

<img width="822" alt="Screenshot 2022-05-18 at 17 29 00" src="https://user-images.githubusercontent.com/4712052/169094354-97736993-8946-47d7-87fa-674cef1f4b10.png">





