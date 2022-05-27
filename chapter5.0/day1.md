**1. Describe what an event is, and why it might be useful to a client.**

An event tells the "outside world" about something important which has happened to an NFT, such as if an NFT has been minted. This is useful for clients so that they can be easily notified when an event like a minting takes place. 

**2. Deploy a contract with an event in it, and emit the event somewhere else in the contract indicating that it happened.**

<img width="433" alt="Screenshot 2022-05-27 at 17 10 17" src="https://user-images.githubusercontent.com/4712052/170737636-7d9b56db-de21-480b-86eb-65d497d0294e.png">

**3. Using the contract in step 2), add some pre conditions and post conditions to your contract to get used to writing them out.**

<img width="673" alt="Screenshot 2022-05-27 at 17 34 53" src="https://user-images.githubusercontent.com/4712052/170741483-f2f5643c-520a-474b-a40e-e06b3c5c1bd1.png">

**4. For each of the functions below (numberOne, numberTwo, numberThree), follow the instructions.**

`numberOne`

Yes, in this case it will log the name because the name Jacob does indeed equal 5 letters. Conversely, if the name was a different length, code will abort or "panic" due to the ternary else condition and will not reach the final instruction to `log` at the end of the function.

`numberTwo`

Yes it will return the value "Jacob Tucker" as entering the Jacob string parameter and concatenating with Tucker will mean that the condition in post will be satisfied.

`numberThree`

I'm not sure about this one to be honest. But I think the code is saying: after numberThree function is run, make sure that the unmodified self.number is equal to the return value `result` plus one. This is not true, because the unmodified variable will always be one less than the returned result. So the code should panic and not log the return value. (Again this was hard to wrap my head around so I could have misunderstood something).

After function is run, the value of `self.number` should just be 1 (result of 0 + 1) as we initialise the variable at 0.
