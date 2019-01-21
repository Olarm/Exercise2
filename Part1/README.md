# Mutex and Channel basics

### What is an atomic operation?
> An operation in which the CPU can both read and write simultaneously, preventing any other process from reading or writing memory

### What is a semaphore?
> A variable or abstract data type used by threads to signal the state of its control of a resource.

### What is a mutex?
> A mutual exclusion key acquired by for example a thread giving it sole access to a resource

### What is the difference between a mutex and a binary semaphore?
> Both a mutex and semaphore excludes all but 1 process from a resource. A mutex is controlled by the controlling thread whereas a semaphore can be controlled by all threads.

### What is a critical section?
> memory area or resource that will not operate correctly if accessed by multiple concurrent accesses.

### What is the difference between race conditions and data races?
 > A data race occurs when 2 instructions from different threads access the same memory location, at least one of these accesses is a write and there is no synchronization that is mandating any particular order among these accesses. A race condition is not as clear-cut, but can for example be applied to a situation where to threads attempt to write the same locked variable. In this case 1 thread will always reach the variable first but which one this is will be unknown before runtime.

### List some advantages of using message passing over lock-based synchronization primitives.
> A thread dying while locking a resource may lock it indefinetely, message passing allows other processes to parttake in arbitration. less risk of deadlocking. Adds overhead, passing resources takes more time?

### List some advantages of using lock-based synchronization primitives over message passing.
> Message passing uses a message buffer which can fill up. Cycli waiting state, A -> B -> C -> A for example. Adds a certain complexity compared to locks where locks is a simpler arbitration.
