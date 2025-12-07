# Data structures:
The OS is a program like no other, and because of that it has key data structures for certain things.
For example to track the state of each process, the OS will likely keep a __process-list__ for all processes that are ready (also additional information to track which process is currently running). 

Figure 4.3 shows what kind of info the OS needs to track each process in the xv6 kernel.
The same principal is applied to windows, linux, mac just a bit more complicated

```c
// the registers xv6 will save and restore
// to stop and subsequently restart a process
struct context {
int eip;
int esp;
int ebx;
int ecx;
int edx;
int esi;
int edi;
int ebp;
};
// the different states a process can be in
enum proc_state { UNUSED, EMBRYO, SLEEPING,
RUNNABLE, RUNNING, ZOMBIE };
// the information xv6 tracks about each process
// including its register context and state
struct proc {
char *mem; // Start of process memory
uint sz; // Size of process memory
char *kstack; // Bottom of kernel stack
              // for this process
enum proc_state state; // Process state
int pid; // Process ID
struct proc *parent; // Parent process
void *chan; // If non-zero, sleeping on chan
int killed; // If non-zero, have been killed
struct file *ofile[NOFILE]; // Open files
struct inode *cwd; // Current directory
struct context context; // Switch here to run process
struct trapframe *tf; // Trap frame for the
                      // current interrupt
};
```
