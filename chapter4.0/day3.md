**1. Why did we add a Collection to this contract? List the two main reasons.**

- We want to use a Collection so that we can have a "wrapper" which contains multiple NFTs belonging to that collection if needed. A simple way to think about this is using a folder in your OS to contain multiple files. (Everything is a lot more organised this way!). In this analogy the collection is the folder, and the NFT is the file.

- Using a collection is also important as it enables a project to create or "mint" an NFT into our account. It is not possible to directly mint an NFT to an account without a collection.

**2. What do you have to do if you have resources "nested" inside of another resource? ("Nested resources")**

With nested resources we must define a destroy function and inside that use the destroy keyword in order to delete the resource after we are finished using it. I believe this is a special security feature with Cadence which prevents us from forgetting to delete a resource which would make it easier for a hacker to steal our precious NFT!

**3. Brainstorm some extra things we may want to add to this contract. Think about what might be problematic with this contract and how we could fix it.**

i.) If everyone can mint an NFT this could potentially mean an unlimited number would be created which would destroy its scarcity and therefore its value. We could limit this by putting a rule in the smart contract to only mint a maximum number of the resource. We could also create a specific time window in which minting is allowed. Or perhaps only a central entity in charge of the collection such as Dapper Labs with NBA Top Shot would be responsible for pre-minting ahead of time before the collection is made available to the public.

ii.) This is not really ideal as usually we want to avoid moving resources around to minimise security vulnerabilities. (The code for this is also quite complex in Flow). Instead we want to create references ie. links to the collection if possible - might this be a possible solution to this issue?

In terms of adding things to the contract, I know this is only a completely stripped down hello world example, but of course we want some actual content for the NFT like an image or video, and not just a uuid!
An additional thing (perhaps less obvious) - we may want some functions which allow us to add (and remove) an accessory like a weareable to the NFT. For example in the upcoming Genies project on Flow you can customise your Avatar NFT by adding pieces of clothing which are also NFTs themselves.




