# os_cheatsheet
What is an operating system?
What are the functions of os ?
What are the different types of operating system ?
What is process State and PCB?
What is the difference between an operating system and a firmware ?
What is the role of a kernel in an operating system ?
What is system call() ?
What is fork() ?
What is the difference between threads and processes?
What is multitasking in an os ?
What is multithreading in an os?
What is a scheduler in os?
What is the difference between preemptive and non preemptive ?
What is the difference between multiprogramming and multitasking ?
What is process synchronisation ?
What is the purpose of virtual memory in an OS ?
What is paging and segmentation in an os ?
What is demand paging in an os ?
What is semaphore in an os ?
What is the difference between a deadlock and a livelock ?
What is the difference between a mutex and a binary semaphore?
What is interrupt handling in an os?
How does an opening system manage I/O operations?
What is the device driver in an os ?
What is file system management in an OS ?
What is virtualization and its type?
What is micro kernel and monolithic kernel ?
What is the chmod command ?
What is internal, external fragmentation?
What is the difference between Spatial locality vs Temporal locality ?
What is meant by virus, worm , Trajan, malware, Spywar
### What is the main purpose of an operating system? Discuss different types? 
 An operating system (OS) is system software that manages computer hardware, software resources, and provides common services for computer programs. So it manages the computer’s memory, processes, devices, files, and security aspects of the system. It also allows us to communicate with the computer without knowing how to speak the computer’s language. Without an operating system, a computer is not useful.

Types of operating system:

Batch OS
Distributed OS
Multitasking OS
Network OS
Real-Time OS
Mobile OS
Reference: https://www.geeksforgeeks.org/types-of-operating-systems/

### What is a socket, kernel and monolithic kernel ?
Socket:
A socket is defined as an endpoint for communication, A pair of processes communicating over a network employ a pair of sockets ,one for each process. A socket is identified by an IP address concatenated with a port number.
The server waits for incoming client requests by listening to a specified port. Once a request is received, the server accepts a connection from the client socket to complete the connection.

Kernel is the central core component of an operating system that manages operations of computer and hardware. Kernel Establishes communication between user level application and hardware. Manages memory and CPU time. Decides state of incoming processes. Controls Disk, Memory, Task Management

Monolithic Kernel (provides good performance but lots of lines of code)
It is one of the types of kernel where all operating system services operate in kernel space. It has dependencies between system components. It has huge lines of code which is complex.
Example : Unix, Linux, Open VMS, XTS-400 etc.
### Difference between process and program and thread? Different types of process. 
Process:
Process is an instance of an executing program. For example, we write our computer programs in a text file and when we execute this program, it becomes a process which performs all the tasks mentioned in the program.

Program:
Program is a set of instructions to perform a certain task. Eg: chrome.exe, notepad.exe

Thread:
Thread is a path of execution within a process. A thread is also known as a lightweight process. The idea is to achieve parallelism by dividing a process into multiple threads. For example,Word processor uses multiple threads: one thread to format the text, another thread to process inputs.
### Define virtual memory, thrashing, threads.  
Virtual Memory:
A computer can address more memory than the amount physically installed on the system. This extra memory is actually called virtual memory and it is a section of a hard disk that’s set up to emulate the computer’s RAM.
The main visible advantage of this scheme is that programs can be larger than physical memory. Virtual memory serves two purposes. First, it allows us to extend the use of physical memory by using a disk. Second, it allows us to have memory protection, because each virtual address is translated to a physical address.

Thrashing:
Thrashing is a condition or a situation when the system is spending a major portion of its time in servicing the page faults, but the actual processing done is very negligible. High degree of multiprogramming(if number of processes keeps on increasing in the memory), lack of frames (if a process is allocated too few frames, then there will be too many and too frequent page faults) causes Thrashing.

Threads:
A thread is a single sequential flow of execution of tasks of a process so it is also known as thread of execution or thread of control.
### What is RAID ? Different types. 
RAID, or “Redundant Arrays of Independent Disks” is a technique which makes use of a combination of multiple disks instead of using a single disk for increased performance, data redundancy or both.Data redundancy, although taking up extra space, adds to disk reliability. This means, in case of disk failure, if the same data is also backed up onto another disk, we can retrieve the data and go on with the operation.
### What is a deadlock? Different conditions to achieve a deadlock. 
A Deadlock is a situation where each of the computer processes waits for a resource which is being assigned to some other process. In this situation, none of the processes gets executed since the resource it needs is held by some other process which is also waiting for some other resource to be released.

How deadlock is achieved: Deadlock happens when Mutual exclusion, hold and wait, No preemption and circular wait occurs simultaneously.

Necessary Conditions for deadlock:

Mutual Exclusion
Hold and Wait
No preemption
Circular Wait
### What is fragmentation? Types of fragmentation. 
Fragmentation:
An unwanted problem in the operating system in which the processes are loaded and unloaded from memory, and free memory space is fragmented. Processes can’t be assigned to memory blocks due to their small size, and the memory blocks stay unused. It is also necessary to understand that as programs are loaded and deleted from memory, they generate free space or a hole in the memory. These small blocks cannot be allotted to new arriving processes, resulting in inefficient memory use.

The conditions of fragmentation depend on the memory allocation system. As the process is loaded and unloaded from memory, these areas are fragmented into small pieces of memory that cannot be allocated to incoming processes. It is called fragmentation.

Types of fragmentation:
1. Internal
2. External
### What is spooling ? 
SPOOL is an acronym for simultaneous peripheral operations online. Spooling is a process in which data is temporarily held to be used and executed by a device, program, or system.
In spooling, there is no interaction between the I/O devices and the CPU. That means there is no need for the CPU to wait for the I/O operations to take place. Such operations take a long time to finish executing, so the CPU will not wait for them to finish.
The biggest example of Spooling is printing. The documents which are to be printed are stored in the SPOOL and then added to the queue for printing. During this time, many processes can perform their operations and use the CPU without waiting while the printer executes the printing process on the documents one-by-one.
### What is semaphore and mutex (Differences might be asked)? Define Binary semaphore. 
Mutex                                      	Semaphore
A mutex is an object.	
Mutex works upon the locking mechanism.	
 A mutex is a type of semaphore that supports mutual exclusion, preventing two threads from operating simultaneously on a particular resource. In addition, it allows only one thread at a time to access the resource. 
Mutex doesn’t have any subtypes.
Operations on Mutex: Lock , Unlock
A mutex can only be modified by the process that is requesting or releasing a resource.
If the mutex is locked then the process needs to wait in the process queue, and mutex can only be accessed once the lock is released.

A semaphore is an integer.Semaphore uses signaling mechanism.A semaphore is a non negetive variable value used for access control mechanism. It is used as a synchronization tool to share information among several processes.
Semaphore work with two atomic operations (Wait, signal) which can modify it.
Operations on mutex: Wait , Signal
Semaphore is of two types:
Counting Semaphore
Binary Semaphore
	If the process needs a resource, and no resource is free. So, the process needs to perform a wait operation until the semaphore value is greater than zero. 

Both semaphores and mutexes are used in computer programming and systems management. 
	
### Belady’s Anomaly
Belady’s anomaly is the name given to the phenomenon where increasing the number of page frames results in an increase in the number of page faults for a given memory access pattern.

Solution to fix Belady’s Anomaly:
Implementing alternative page replacement algo helps eliminate Belady’s Anomaly.. Use of stack based algorithms, such as Optimal Page Replacement Algorithm and Least Recently Used (LRU) algorithm, can eliminate the issue of increased page faults as these algorithms assign priority to pages.
### Starving and Aging in OS
Starving/Starvation(also called Lived lock): Starvation is the problem that occurs when low priority processes get jammed for an unspecified time as the high priority processes keep executing. So starvation happens if a method is indefinitely delayed.

Solution to Starvation : Ageing is a technique of gradually increasing the priority of processes that wait in the system for a long time.
### Why does trashing occur? 
High degree of multiprogramming(if number of processes keeps on increasing in the memory) , lack of frames(if a process is allocated too few frames, then there will be too many and too frequent page faults.) causes Thrashing.
### What is paging and why do we need it? 
Paging is a memory management scheme that eliminates the need for contiguous allocation of physical memory. This scheme permits the physical address space of a process to be non – contiguous.
Paging is used for faster access to data. When a program needs a page, it is available in the main memory(RAM) as the OS copies a certain number of pages from your storage device to main memory. Paging allows the physical address space of a process to be noncontiguous.
### Demand Paging, Segmentation 
Demand paging is a method of virtual memory management which is based on the principle that pages should only be brought into memory if the executing process demands them. This is often referred to as lazy evaluation as only those pages demanded by the process are swapped from secondary storage to main memory.
So demand paging works opposite to the principle of loading all pages immediately.

Segmentation is a memory management technique in which the memory is divided into the variable size parts. Each part is known as a segment which can be allocated to a process.

The details about each segment are stored in a table called a segment table. Segment table is stored in one (or many) of the segments.

Segment table contains mainly two information about segment:

Base: It is the base address of the segment
Limit: It is the length of the segment.
### Real Time Operating System, types of RTOS. 
A real-time operating system (RTOS) is a special-purpose operating system used in computers that has strict time constraints for any job to be performed and is intended to serve real time applications that possess data as it comes in , typically without buffer delays.

Types of RTOS:

Hard RTOS
Firm RTOS
Soft RTOS
### Difference between main memory and secondary memory. 
### Static Binding vs Dynamic Binding 
Static binding happens when the code is compiled, while dynamic bind happens when the code is executed at run time.

Static Binding:
When a compiler acknowledges all the information required to call a function or all the values of the variables during compile time, it is called “static binding”. As all the required information is known before runtime, it increases the program efficiency and it also enhances the speed of execution of a program. Static Binding makes a program very efficient, but it declines the program flexibility, as ‘values of variable’ and ‘function calling’ are predefined in the program. Static binding is implemented in a program at the time of coding. Overloading a function or an operator is the example of compile time polymorphism i.e. static binding.

Dynamic Binding Calling a function or assigning a value to a variable, at run-time is called “Dynamic Binding”. Dynamic binding can be associated with run time ‘polymorphism’ and ‘inheritance’ in OOP. Dynamic binding makes the execution of a program flexible as it can decide what value should be assigned to the variable and which function should be called, at the time of program execution. But as this information is provided at run time it makes the execution slower as compared to static binding.
## Scheduling
### FCFS Scheduling 
### SJF Scheduling 
### SRTF Scheduling 
### LRTF Scheduling 
### Priority Scheduling 
### Round Robin Scheduling 
### Producer Consumer Problem 
About Producer-Consumer problem: The Producer-Consumer problem is a classic problem that is used for multi-process synchronisation i.e. synchronisation between more than one processes.

The job of the Producer is to generate the data, put it into the buffer, and again start generating data. While the job of the Consumer is to consume the data from the buffer.

What’s the problem here?
The following are the problems that might occur in the Producer-Consumer:

The producer should produce data only when the buffer is not full. If the buffer is full, then the producer shouldn’t be allowed to put any data into the buffer.
The consumer should consume data only when the buffer is not empty. If the buffer is empty, then the consumer shouldn’t be allowed to take any data from the buffer.
The producer and consumer should not access the buffer at the same time.

We can solve this problem by using semaphores.
### Banker’s Algorithm 
It is a banker algorithm used to avoid deadlock and allocate resources safely to each process in the computer system. The ‘S-State’ examines all possible tests or activities before deciding whether the allocation should be allowed to each process. It also helps the operating system to successfully share the resources between all the processes. The banker’s algorithm is named because it checks whether a person should be sanctioned a loan amount or not to help the bank system safely simulate allocation resources.
### Explain Cache
### Diff between direct mapping and associative mapping 
### Diff between multitasking and multiprocessing 
