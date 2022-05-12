### Define your own contract that stores a dictionary of resources. Add a function to get a reference to one of the resources in the dictionary.

<img width="517" alt="Screenshot 2022-05-12 at 17 05 32" src="https://user-images.githubusercontent.com/4712052/168120978-484677b8-d5f5-40f9-a07d-87b051ecabfe.png">

### Create a script that reads information from that resource using the reference from the function you defined in part 1.

<img width="604" alt="Screenshot 2022-05-12 at 17 11 23" src="https://user-images.githubusercontent.com/4712052/168121014-f001cd1f-dcda-41aa-901b-4d82b349f6db.png">

### Explain, in your own words, why references can be useful in Cadence.

It is much easier to create a reference for complex data structures like structs or resources rather than moving the data around to get access to specific attributes at different places in your project. This is particularly useful for resources since Cadence makes it deliberately difficult to move this valuable data around for security reasons ie. to avoid loss of a valuable asset.



