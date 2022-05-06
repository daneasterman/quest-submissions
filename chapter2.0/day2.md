### 1. Explain why we wouldn't call changeGreeting in a script.

This is because scripts are only used to view or "read" things on the blockchain while transactions are used to modify (write) or make changes to the smart contract.

### 2. What does the AuthAccount mean in the prepare phase of the transaction?

`AuthAccount` is used to access data in a web3 wallet account. When the user confirms or signs a transaction in their web3 wallet, "behind the scenes" our code is using the AuthAccount type to authorise the transaction.

### 3. What is the difference between the prepare phase and the execute phase in the transaction?

The prepare phase is used to conduct the authentication stage of the transaction. In other words, this is the step whereby the user approves access to his/her account.

By contrast the execute phase does not handle authentication but rather does all the other main modification work involved with executing all our functions. 

The prepare/execute distinction is a useful way to keep our code clean and follow the general coding principle of "separation of concerns". 

**Coding sub-tasks**

_i.) A variable named myNumber that has type Int (set it to 0 when the contract is deployed):_
(See contract screenshot below)

_ii.) A function named updateMyNumber that takes in a new number named newNumber as a parameter that has type Int and updates myNumber to be newNumber_
(See contract screenshot below)

<img width="478" alt="Screenshot 2022-05-06 at 11 07 07" src="https://user-images.githubusercontent.com/4712052/167117589-ddbeaf67-2e67-4373-8efc-a1a381fc485e.png">

iii.) _Add a script that reads myNumber from the contract_:

<img width="362" alt="Screenshot 2022-05-06 at 11 17 32" src="https://user-images.githubusercontent.com/4712052/167117740-8b28cd0a-642e-4b22-93bf-e07c57741e53.png">

Note, as you can see in the script output below, initially I tried to name two functions with different names to return both the greeting and myNumber variables. Is "main" only reserved for this purpose? - as the error said  "missing entry point, expected main".

<img width="820" alt="Screenshot 2022-05-06 at 11 18 11" src="https://user-images.githubusercontent.com/4712052/167117890-7935609a-f543-4ffa-b334-aecc1479a3fd.png">

_iv.) Add a transaction that takes in a parameter named myNewNumber and passes it into the updateMyNumber function. Verify that your number changed by running the script again._

<img width="431" alt="Screenshot 2022-05-06 at 11 22 48" src="https://user-images.githubusercontent.com/4712052/167117998-a2412484-a3e3-4620-8891-9e3086bb8587.png">

<img width="499" alt="Screenshot 2022-05-06 at 11 23 48" src="https://user-images.githubusercontent.com/4712052/167118019-06558674-7bdc-4224-a0f4-5750d3da2c4f.png">

