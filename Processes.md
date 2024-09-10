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
      - Some hardware provides multiple sets of registers per CPU
          - Allows multiple contexts to be loaded at once

