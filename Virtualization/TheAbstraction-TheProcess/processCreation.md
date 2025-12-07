# Process creation (In a little bit more detail.)

# So how does a process grab a program up and running?
First of all the program needs to __load__ the code and static data (e.g. initialized memory )into memory, into the address space of the process.
Programs initially reside on the disk as executable formats; thus the program needs to read the bytes of the program and put them into memory.

# there are 2 ways to do this:

## eagerly (Old OS solution):
The OS puts all the bytes to memory at once.
## lazy way (lazier solution):
Loading pieces of the code into memory when required by the program execution.
(To truly understand how this works we'll need to know paging and swapping; topics which will be covered in later chapters.).


# what now?
Once the OS put the code and static data into memory it needs to do a few other things.

Some memory needs to be allocated to the run-time stack/stack.
As you know C programs use the stack for allocating local variables,function parameters and local addresses; the OS allocates this memory and gives it to the process. 
The OS will also likely initialize the stack with arguments.

Specifically it will fill in the arguments of main() i.e argc and argv

The OS will also initialize space for the programs heap.
The OS will also create initialization tasks specifically for I/O

After loading static data and code into memory, initializing the stack and the heap, and create initialization for I/O the process can finally start
