**Preemptive and Nonpreemptive Scheduling**

Nonpreemptive scheduling:
- Once the CPU has been allocated to a process, the process keeps the CPU until it releases it either by terminating or by switching to the waiting state.

Preemptive scheduling:
- Preemptive scheduling can result in race conditions
when data are shared among several processes.
- Consider the case of two processes that share data.
While one process is updating the data, it is preempted
so that the second process can run. The second process
then tries to read the data, which are in an inconsistent
state.
