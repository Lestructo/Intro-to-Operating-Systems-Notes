Stack >> Function

Processes and Memory
- Text: Storage of code
- Date: Global variables (pre-allocated space)
- Heap: Dynamically allocated space
- Stack: Local variable storage

Stack and Heap
- Stack grows downward with each nested function call
    - Local variables, register state, return memory address
- Heap
    - Storage of dynamically allocated items that must be persistent across function calls (and returns from function calls)
    - OOP Languages: Object instantiation is done in the heap
 
Process State: A process is in exactly one state at any instance in time.

Context Switching
- When CPU switches to another process, the system must save the state of the old process and load the saved state for the new process via a context switch.
- Context of a process represented in the PCB
- Context-switch time is overhead; the system does no useful work while switching
    - The more complex the OS and the PCB, the longer the context switch
    - Time is dependent on hardware support
    - Some hardware provides multiple sets of registers per CPU (allows multiple contexts to be loaded at once)


**Process Creation**

- Parent process creates child processes, which, in turn, create other processes forming a tree of processes
- Generally, process identified and managed via a process identifier (pid)

Resource sharing options
- Parent and children share all resources
- Children share subset of parent’s resources
- Parent and child share no resources

Execution options
- Parent and children execute concurrently
- Parent waits until children terminate

Process Termination
- Process executes the last statement and then asks the OS to delete it using the exit() system call.
- Some operating systems do not allow child processes to exist if its parent has terminated (including Linux). If a process terminates, then all its children must also be terminated.
- If parent is executing, but not waiting (did not invokewait()) and the child process ends, then the child process is a zombie.
- If parent terminated without invoking wait(), the child process is an orphan.

Cooperating Processes
- Independent process cannot affect or be affected by the execution of another process
- Cooperating process can affect or be affected by the execution of another process
- Advantages of process cooperation: Information sharing, Computation speed-up, Modularity, Convenience
