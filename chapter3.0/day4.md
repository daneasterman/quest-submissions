### 1. Explain, in your own words, the 2 things resource interfaces can be used for (we went over both in today's content)

- Interfaces allow us to define a specification for how a struct or resource can be used.

- An interface can be used to decide whether or not to expose a specific function or data type when it comes to implementing a struct or resource later in our code.

### 2. Define your own contract. Make your own resource interface and a resource that implements the interface. Create 2 functions. In the 1st function, show an example of not restricting the type of the resource and accessing its content. In the 2nd function, show an example of restricting the type of the resource and NOT being able to access its content.

The contract with the `accessKittyString` function below is allowed to access the Kitty resource's string content as it is defined in the Interface. This also means that the contract can be deployed.

<img width="609" alt="Screenshot 2022-05-13 at 12 02 47" src="https://user-images.githubusercontent.com/4712052/168270427-d6f2d110-38f5-4dc1-96d8-de36fb0800f8.png">

In the screenshot below with the `noAccessKittyInteger` function I cannot access the `catMintCount` data because while it has been defined in the resource itself, it has not been defined in the resource interface. This gives me the error: `"member of restricted type catMintCount is not accessible"`, which also means the contract cannot be deployed.

<img width="693" alt="Screenshot 2022-05-13 at 12 05 21" src="https://user-images.githubusercontent.com/4712052/168270750-9da95b29-0eb7-45be-9824-e65a2c984f23.png">

### 3. How would we fix this code?

#### i.) ERROR: structure Stuff.Test does not conform to structure interface Stuff.ITest`

Here we need to add the `favouriteFruit` string attribute to the struct as it is missing in the example. 
So to fix we would add: `pub var favouriteFruit: String` in the struct.

#### ii.) ERROR HERE: `member of restricted type is not accessible: changeGreeting`
This time the changeGreeting function is not defined in the struct interface.

To fix we add: `pub fun changeGreeting(newGreeting: String): String` inside the struct interface. 

