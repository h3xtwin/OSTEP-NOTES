# Introduction to operating systems:
a running program does one very simple thing, executes instructions, millions and billions of instructions.
The __processor__ *fetches* an instruction from memory, decodes it, and executes it.
After it is done it moves on to the next instruction. then the other, and other and other.
Thus we have just described the basics of the __Von Neumann__ model of computing.
This might sound simple, but in this class we will be learning what's going on while a program runs, a lot of wild things are going on with the primary goal of making the system __easy to use__

There is a body of software that's responsible for making it simple programs, allowing to share memory, enabling programs to interact with devices, and other fun stuff like that.
That body of software is called the __operating system (OS)__


## Continuation:
The primary way the OS does this is through a technique we call __virtualization__. That is, the OS takes a __physical__ resource (such as a processor, disk, or memory) and transforms it into a more general, powerful and easy to use virtual form of itself.
Thus, we sometimes refer to the operating system as a virtual machine.

the OS also provides some interfaces (APIS) that you can call.
a typical OS in fact exports a few hundred __syscalls__ that are available to applications.
