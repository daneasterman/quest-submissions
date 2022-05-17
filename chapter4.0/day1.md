**1. Explain what lives inside of an account.**
Inside an account you can have multiple smart contracts and you can store resources such as NFTs. 

**2. What is the difference between the /storage/, /public/, and /private/ paths?**
The `/storage/` path is completely private and can nonly be acccessed by the owner of the account. As the name suggests, `/public/` path is accessible to anyone and finally the `/private/` path only provides access to the account owner or to someone the owner explicitly grants access rights.

**3. What does `.save()` do? What does `.load()` do? What does `.borrow()` do?**
i.) `.save()` saves a resource to an account.
ii.) `.load()` loads or extracts a resource from an account.
iii.) `.borrow()` does not actually extract or move the resource out of the account but instead is used so we can view the resource.

**4. Explain why we couldn't save something to our account storage inside of a script.**

Scripts only allow us to view things on the blockchain. The save operation means we are modifying or writing something on the blockchain which can only be done in the smart contract or transaction.

**5. Explain why I couldn't save something to your account.**

The only way that something can be saved to the account is if the account owner authorises it by signing the transaction. (This is why you must be very careful when you click the "sign" button in your web3 wallet).

**6. Define a contract that returns a resource that has at least 1 field in it. Then, write 2 transactions:**

<img width="359" alt="Screenshot 2022-05-17 at 18 02 56" src="https://user-images.githubusercontent.com/4712052/168870280-69fffa00-edc8-43b6-95f7-eedbce3bac33.png">

**i.) A transaction that first saves the resource to account storage, then loads it out of account storage, logs a field inside the resource, and destroys it.**

<img width="766" alt="Screenshot 2022-05-17 at 18 18 41" src="https://user-images.githubusercontent.com/4712052/168872848-d3bbd2a9-2235-4494-a614-600b69678435.png">

**ii.) A transaction that first saves the resource to account storage, then borrows a reference to it, and logs a field inside the resource.**

<img width="769" alt="Screenshot 2022-05-17 at 18 23 03" src="https://user-images.githubusercontent.com/4712052/168873580-062d2b8c-5fc7-4918-b3a8-bb54e1cfc3eb.png">

