**1. Variable a**

This variable can be read and written to everywhere ie. at all scopes both in the code for the smart contract, scripts and transactions. As a result this is the least secure access control type.

**2. Variable b**

Can be read at all scopes including in scripts and transactions, but can only be written at the local scope where it is defined.

**3. Variable c**

Can only be read within the contract (not in scripts or transactions), and like variable b can only be written at the local scope where is defined.

**4. Variable d**

Can only be read and written at the local scope where it is defined.

**1. publicFunc**

This function can be called anywhere including in the contract, transactions and scripts.

**2. contractFunc**

Can only be called inside the smart contract.

**3. privateFunc**

Can only be called at the local scope where it is defined.














