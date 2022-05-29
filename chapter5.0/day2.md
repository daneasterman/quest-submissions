**1. Explain why standards can be beneficial to the Flow ecosystem.**

It means that third party Dapps like an NFT marketplace do not have write custom code for every single new NFT project which wants to list or interact with that Dapp. These Dapps should not have to reinvent the wheel as there are certain common functions such as deposit and withdraw which will needed every time. As the classic programmer's refrain goes: "Don't repeat yourself"!

**2. What is YOUR favourite food?**

Haha this would really not make sense to me if I hadn't watched the video! I'll try to be more creative than Jacob ;-) - I like Korean, Persian and Italian food the most!

**3. Please fix this code (Hint: There are two things wrong):**

i.) In the updateNumber function in the implementing contract we didn't set `self.number` to the `newNumber` parameter. (We hardcoded it to 5).

ii.) Again in the implementing contract we defined our own IStuff resource interface when we should have used the resource interface from the contract interface, something like: `ITest.IStuff`.



