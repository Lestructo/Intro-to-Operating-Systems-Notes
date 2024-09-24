**Pipes**
Act as a conduit allowing two processes on the same computer to communicate.
Issues:
– Is communication unidirectional or bidirectional?
– In the case of two-way communication, is it half or
full-duplex?
– Must there exist a relationship (i.e., parent-child)
between the communicating processes?
– Can the pipes be used over a network?

Ordinary pipes:
- Cannot be accessed from outside the process that created it.
- Parent creates the process and then forks()
- Both parent and child close one half of the pipe so there is only one reader and one writer for the pipe.
- When the producer closes the fd, the bytes in the buffer are still available for reading
- Typically, a parent process creates a pipe and uses it to communicate with a child process that it created.

Named pipes:
- Can be accessed without a parent-child relationship.
- One process opens for reading, the other for closing
- open() system call blocks until the other process also calls open()
- When the producer closes, the bytes in the pipe’s buffer are still available for reading

