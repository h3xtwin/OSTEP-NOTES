In this chapter we'll discuss the most fundamental abstraction the OS provides:
  => The process!!! <=

# What is a process?
__A running program.__

The program by itself is a lifeless thing; it just sits there on the disk like a dumb ass on the disk with a bunch of instructions (and maybe some static data) waiting to spring into action.
It is the __OS__ that takes those bytes and puts them into action.

## but:
it seems more than often a user wants to have more than one process running.
For example on a PC a user might want open:
- a browser
- a mail app
- angry birds idk
- steam
- call of booty black cocks 

In fact, a typical system may be seemingly running tens or even hundreds of processes at the same time.
Doing so makes the system very easy to use, as one never needs to be concerned with whether the CPU is available.

one simply runs a program.
## Which hence the challenge:
- how to simulate many CPUS?

The OS creates the illusion of __infinite CPUS__ with virtualization.
- running a one process
- stopping
- running another
- and so fourth
This technique ^^^ is known as __time sharing__ of the CPU, allows users to run as many concurrent processes as they want; the only potential cost is performance, as each process the CPU will have to iterate through for a longer time.

To implement Virtualization of the CPU and to implement it well, the OS will need both some low level machinery and some high level intelligence
We call the low level machinery __mechanisms__; mechanisms are low level methods or protocols that implement a needed piece of functionality

# TIP: USE OF TIME SHARING:
__time sharing__ is a basic technique used by the OS to share a resource.
The way time sharing works is for allowing a resource to be used for a little while by one entity and then a little while and so fourth.
The counterpart of time sharing is __space sharing__, where a resource is divided (in space) among those who wish to use it.
For example, disk space is naturally a space shared resource; once a block is a assigned to a file it is normally not assigned to another file until the user deletes the original file.


