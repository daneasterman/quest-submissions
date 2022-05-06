### In a script, initialize an array (that has length == 3) of your favourite people, represented as Strings, and log it.

<img width="536" alt="Screenshot 2022-05-06 at 12 42 32" src="https://user-images.githubusercontent.com/4712052/167164534-6bbc2f13-44a9-4e5f-bfb7-c4bba71edfb3.png">

<img width="481" alt="Screenshot 2022-05-06 at 12 42 38" src="https://user-images.githubusercontent.com/4712052/167164643-3bb5d4e5-edac-437c-a8ff-14d537833875.png">

**In a script, initialize a dictionary that maps the Strings Facebook, Instagram, Twitter, YouTube, Reddit, and LinkedIn to a UInt64 that represents the order in which you use them from most to least. For example, YouTube --> 1, Reddit --> 2, etc. If you've never used one before, map it to 0!**

<img width="1010" alt="Screenshot 2022-05-06 at 12 52 37" src="https://user-images.githubusercontent.com/4712052/167164688-3b5c80d0-ca65-4ae4-99c2-4b545b7e50ed.png">

<img width="867" alt="Screenshot 2022-05-06 at 12 52 44" src="https://user-images.githubusercontent.com/4712052/167164705-71dbb53c-383c-4412-8bd4-53ad502e44f7.png">

**Explain what the force unwrap operator ! does, with an example different from the one I showed you (you can just change the type).**

The force-unwrap operator unwraps an optional type. If there is indeed a value with a type it will successfully unwrap, but if the value is nil the program will stop - and probably throw a big error message!

Example unwrapping Optional Array instead of Optional String:

<img width="1164" alt="Screenshot 2022-05-06 at 13 05 35" src="https://user-images.githubusercontent.com/4712052/167165073-2e13cae0-79d0-4582-8672-d95fbd3855d0.png">

**Using the picture , explain...**

_i.) What the error message means_

The return type of the function is a string but what we are actually getting is an "optional String" (which can be a String or Nil).

ii.) *Why we're getting this error*

We're getting this because with Cadence when you access a value in a dictionary you will always get an optional.

iii.) *How to fix it*

We can fix this by using the ! force-unwrap operator when returning the value to "convert" it to a "normal" String type.

