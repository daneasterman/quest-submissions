### 1. In words, list 3 reasons why structs are different from resources.

1. Structs can be copied 
2. Structs can be overwritten
3. Structs can be easily created (whenever we want).

### 2. Describe a situation where a resource might be better to use than a struct.

Structs behave more like "traditional" computer data structures which can be easily copied and overwritten. 

We don't want these characteristics when dealing with digital assets like crypto tokens or NFTs which have monetary value. So when dealing with anything which could potentially represent a valuable digital asset like an NFT we would want to use a resource.

### 3. What is the keyword to make a new resource?

`create`

### 4.Can a resource be created in a script or transaction (assuming there isn't a public function to create one)?

No, resources can only be created inside the contract. Scripts are only used for "read" functions in general anyway. I gather that Structs can be created in a transaction as opposed to resources which may not.


### 5. What is the type of the resource below?

```
pub resource Jacob {

}

```
^^ This resource is of type "Jacob".


### Let's play the "I Spy" game from when we were kids. I Spy 4 things wrong with this code. Please fix them.

i.) No `@` symbol is used to highlight that the type we are using in the function is a resource.

ii.) We are copying resource `Jacob()` to a new variable `myJacob` which is not allowed. It must be explicitly moved. Also we are not using the explicit `create` keyword.

iii.) Again we cannot do a normal return but must use the `<-` move operator which makes it easier for us to keep track of what we are doing with the (potentially) valuable resource.
