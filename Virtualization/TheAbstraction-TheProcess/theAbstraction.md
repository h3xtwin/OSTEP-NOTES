# the abstraction

The abstraction provided by the OS is something we will refer to as a __process__
As we said before a process is simply a running program

to understand what constitutes a process we thus have to understand its __machine state__
one obvious state that compromises a process is its memory.
Instructions lie in memory, the data that the running program reads and writes sits in memory as well
THUS, the memory the process can ADDRESS `thus being called an __ADDRESS SPACE__` is part of the process.
also a part of the process's machine state are __registers__.
Many instructions just read or write registers; thus they are clearly important to a process.
!! NOTE THAT THERE A SPECIAL REGISTERS THAT FORM PART OF THIS MACHINE STATE  (program counter [PC] <sometimes called instruction pointer or IP>) which tells us which instruction of the program will execute next; similarly a __stack pointer__ and associated __frame pointer__ are used to manage the stack for function parameters, local variables and return addresses.

Processes also often access persistant storage devices too. Such I/O information might include a list of the files the process currently has open.
