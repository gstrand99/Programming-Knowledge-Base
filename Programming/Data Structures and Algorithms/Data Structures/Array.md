## What is an array?
- const a = [] isn't an array in js
	- ![[JS ArrayList.png]]
- unbreaking memory space with bites in between
- arrays are not the same as lists
- array's in JS are not the same as they are in something like C

### Getting a specific index
- [[Big O]] of getting something from an array O of 1 or constant time

![[Array image.png]]
- this was an 8 bit array buffer, in the 3rd option you are jumping to the end because you are using 16 bit
- takes the width of the type, multiply by the offset, puts it at the memory address, and you can go get it

### Inserting at a  specific index
- array doesn't grow, it overwrites 

### Deletion at a specific index
- special because you cant fully dealicate  memory from an array
- you will overwrite it with something so you know there is nothing there