# os_cheatsheet
### What is an operating system?
### What are the functions of os ?
### What are the different types of operating system ?
### What is process State and PCB?
### What is the difference between an operating system and a firmware ?
### What is the role of a kernel in an operating system ?
### What is system call() ?
### What is fork() ?
### What is the difference between threads and processes?
### What is multitasking in an os ?
### What is multithreading in an os?
### What is a scheduler in os?
### What is the difference between preemptive and non preemptive ?

### What is process synchronisation ?
### What is the purpose of virtual memory in an OS ?

### What is the difference between a deadlock and a livelock ?
### What is interrupt handling in an os?
### How does an opening system manage I/O operations?
### What is the device driver in an os ?
### What is file system management in an OS ?
### What is virtualization and its type?
### What is micro kernel and monolithic kernel ?
### What is the chmod command ?
### What is internal, external fragmentation?
### What is the difference between Spatial locality vs Temporal locality ?
### What is meant by virus, worm , Trajan, malware, Spywar
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
Different Types of CPU Scheduling Algorithms
 CPU scheduling algorithms 
### First Come First Serve (FCFS) Scheduling Algorithm
The FCFS algorithm is the simplest of scheduling algorithms in OS. This is because the deciding principle behind it is just as its name suggests- on a first come basis. The job that requests execution first gets the CPU allocated to it, then the second, and so on.

Characteristics of FCFS scheduling algorithm

The algorithm is easy to understand and implement.
Programs are executed on a first come first serve basis.
It is a non-preemptive scheduling algorithm.
In this case, the ready queue acts as the First In First Out (FIFO) queue - Where the job that gets ready for execution first, also gets out first.
This is used in most batch OS.
Advantages of FCFS scheduling algorithm
The fact that it is simple to implement means it can easily be integrated into a pre-existing system.
It is especially useful when the processes have a large burst time since there is no need for context switching.
The absence of low or high-priority preferences makes it fairer.
Every process gets its chance to execute.
Disadvantages of the FCFS scheduling algorithm
Since its first come basis, small processes with a very short execution time, have to wait their turn.
There is a high wait and turnaround time for this scheduling algorithm in OS.
All in all, it leads to inefficient utilization of the CPU.
Example of FCFS scheduling algorithm in OS-

FCFS Scheduling Algorithm in OS Example

In the table above, 5 processes have arrived at the CPU at different times. The process with the minimal arrival time goes first. Since the first process has a burst time of 3, the CPU will remain busy for 3 units of time, which indicates that the second process will have to wait for 1 unit of time since it arrives at T=2. In this way, the waiting and turnaround times for all processes can be calculated. This also gives the average waiting time and the average turnaround time. We can contrast this with other algorithms for the same set of processes.

Using a queue for the execution of processes is helpful in keeping track of which process comes at what stage. Although this is one of the simplest CPU scheduling algorithms, it suffers from the convoy effect. This occurs when multiple smaller processes get stuck behind a large process, which leads to an extremely high average wait time. This is similar to multiple cars stuck behind a slow-moving truck on a single-lane road.

### Shortest Job First (SJF) Scheduling Algorithm
The Shortest Job First (SJF) is a CPU scheduling algorithm that selects the shortest jobs on priority and executes them. The idea is that jobs with short burst time get done quickly, making CPU available for other, longer jobs/ processes. In other words, this is a priority scheduling algorithm based on the shortest burst time.

Characteristics of SJF scheduling algorithm

This CPU scheduling algorithm has a minimum average wait time since it prioritizes jobs with the shortest burst time.
If there are multiple short jobs, it may lead to starvation.
This is a non-preemptive scheduling algorithm.
It is easier to implement the SJF algorithm in Batch OS.
Advantages of SJF scheduling algorithm

It minimizes the average waiting time and turnaround time.
Beneficial in long-term scheduling.
Is better than the FCFS scheduling algorithm.
Useful for batch processes.
Disadvantages of the SJF scheduling algorithm

As mentioned if short time jobs keep on coming, it may lead to starvation for longer jobs.
Is dependent upon burst time, but it is not always possible to know the burst time beforehand.
Does not work for interactive systems.
Example of SJF scheduling algorithm in OS-

SJF scheduling algorithm example

Here, the first 2 processes are executed as they come, but when the 5th process comes in, it instantly jumps to the front of the queue since it has the shortest burst time. The turnaround time and waiting time is calculated accordingly. It's visible that this is an improvement over FCFS, as it smaller average waiting time as well as a smaller average turnaround time. This algorithm is especially useful in cases where there are multiple incoming processes and their burst time is known in advance. The average waiting time obtained is lower as compared to the first-come-first-served scheduling algorithm.

### Longest Job First (LJF) Scheduling Algorithm
The Longest Job First scheduling algorithm is the opposite of SJF scheduling in OS. This algorithm calls for jobs with the longest burst time to be executed first, and then move on to jobs with short burst time.

Characteristics of LJF Scheduling Algorithm

Incoming execution requests are sorted on the basis of burst time in descending order.
It is a non-preemptive CPU scheduling algorithm.
If two jobs have the same burst time, then FCFS is followed.
This priority scheduling in OS is both non-preemptive and preemptive.
Advantages of LJF Scheduling Algorithm

The longest job gets done on priority. That is, no other job gets executed until the longest one completes the execution phase.
Disadvantages of LJF Scheduling Algorithm

It may cause starvation in jobs with a short burst time.
The average waiting and turnaround time is high.
The CPU needs to know the burst time beforehand which is not always possible.
Example of LJF Scheduling Algorithm in OS-

LJF Scheduling Algorithm Example

The first process is executed first, then there is a choice between selecting the second or third process. The third one is selected since it has a higher burst time. Then the fourth one gets executed since it also has a higher burst time than the second process. Finally, the second process gets its chance to go. This approach of CPU scheduling leads to very high waiting times since shorter processes might have to wait for a long period of time to get executed. This also causes the aforementioned convoy effect.

### Priority Scheduling Algorithm in OS
This CPU scheduling algorithm in OS first executes the jobs with higher priority. That is, the job with the highest priority gets executed first, followed by the second prioritized jobs, and so on.

Characteristics of Priority Scheduling Algorithm

Jobs are scheduled on the basis of the priority level, in descending order.
If a job with higher priority than the one running currently comes on, the CPU preempts the current job in favor of the one with higher priority.
But for other purposes, it follows a non-preemptive scheduling approach.
In between two jobs with the same priority, the FCFS process decides which jobs get executed first.
The priority of a process can be set depending on multiple factors like memory requirements, required CPU time, etc.
Advantages of Priority Scheduling Algorithm

This process is simpler than most other scheduling algorithms in OS.
Priorities help in sorting the incoming processes.
Works well for static and dynamic environments.
Disadvantages of Priority Scheduling Algorithm

It may lead to the starvation problem in jobs with low priority.
The average turnaround and waiting time might be higher in comparison to other CPU scheduling algorithms.
Example of Priority Scheduling Algorithm in OS-

Priority Scheduling Algorithm Example

Here, different priorities are assigned to the incoming processes. The lower the number, the higher the priority. The 1st process to be executed is the second one, since it has higher priority than the first process. Then the fourth process gets its turn. This is known as priority scheduling. The calculated times may not be the lowest but it helps to prioritize important processes over others.

### Round Robin Scheduling Algorithm in OS
In this scheduling algorithm, the OS defines a quantum time or a fixed time period. And every job is run cyclically for this predefined period of time, before being preempted for the next job in the ready queue. The jobs that are preempted before completion go back to the ready queue to wait their turn. It is also referred to as the preemptive version of the FCFS scheduling algorithm in OS.

Example of Round Robin Scheduler

As seen from the figure, the scheduler executes the 3 incoming processes part by part.

Characteristics of RR Scheduling Algorithm

Once a job begins running, it is executed for a predetermined time and gets preempted after the time quantum is over.
It is easy and simple to use or implement.
The RR scheduling algorithm is one of the most commonly used CPU scheduling algorithms in OS.
It is a preemptive algorithm.
Advantages of RR Scheduling Algorithm

This seems like a fair algorithm since all jobs get equal time CPU.
Does not lead to any starvation problems.
New jobs are added at the end of the ready queue and do not interrupt the ongoing process.
Leads to efficient utilization of the CPU.
Disadvantages of RR Scheduling Algorithm

Every time job runs the course of quantum time, a context switch happens. This adds to the overhead time, and ultimately the overall execution time.
A low slicing time may lead to low CPU output.
Important tasks aren’t given priority.
Choosing the correct time quantum is a difficult job.
Example of RR Scheduling Algorithm in OS-

RR scheduling algorithm example

Let's take a quantum time of 4 units. The first process will execute and get completed. After a gap of 1 unit, the second process executes for 4 units. Then the third one executes since it has also arrived in the ready queue. After 4 units, the fourth process executes. This process keeps going until all processes are done. It is worth noting that the minimum average waiting time is higher than some of the other algorithms. While this approach does result in a higher turnaround time, it is much more efficient in multitasking environments in comparison to most other scheduling algorithms in OS.

### Shortest Remaining Time First (SRTF) Scheduling Algorithm
The SRTF scheduling algorithm is the preemptive version of the SJF scheduling algorithm in OS. This calls for the job with the shortest burst time remaining to be executed first, and it keeps preempting jobs on the basis of burst time remaining in ascending order.

Characteristics of the SRTF Scheduling Algorithm

The incoming processes are sorted on the basis of their CPU-burst time.
It requires the least burst time to be executed first, but if another process arrives that has an even lesser burst time, then the former process will get preempted for the latter.
The flow of execution is- a process is executed for some specific unit of time and then the scheduler checks if any new processes with even shorter burst times have arrived.
Advantages of SRTF Scheduling Algorithm

More efficient than SJF since it's the preemptive version of SJF.
Efficient scheduling for batch processes.
The average waiting time is lower in comparison to many other scheduling algorithms in OS.
Disadvantages of SRTF Scheduling Algorithm

Longer processes may starve if short jobs keep getting the first shot.
Can’t be implemented in interactive systems.
The context switch happens too many times, leading to a rise in the overall completion time.
The remaining burst time might not always be apparent before the execution.
Example of SRTF scheduling algorithm in OS-

SRTF Scheduling Algorithm Example

Here, the first process starts first and then the second process executes for 1 unit of time. It is then preempted by the arrival of the third process which has a lower service time. This goes on until the ready queue is empty and all processes are done executing.

### Longest Remaining Time First (LRTF) Scheduling Algorithm
This CPU scheduling algorithm is the primitive version of the LJF algorithm. It calls for the execution of the jobs with the longest remaining burst time on a priority basis.

Characteristics of LRTF Scheduling Algorithm

The incoming processes are sorted on the basis of their burst time, in descending order.
It schedules the jobs with longer remaining burst time, first.
The CPU scheduler keeps checking for new jobs with long burst times in regular intervals. And then preempts the current job in favor of other longer burst time remaining jobs.
Advantages of LRTF Scheduling Algorithm

More efficient than LJF since it is the preemptive version of the same.
Almost all jobs get done at the same time, approximately.
Prioritizes longer jobs first, leaving shorter ones for later.
Disadvantages of LRTF Scheduling Algorithm

The average waiting and turnaround time is extremely high.
Shorter jobs may be neglected in favor of longer ones; which may cause starvation.
Burst time has to be known beforehand.
Example of LRTF scheduling algorithm in OS-

LRTF Scheduling Algorithm Example

The first process executes for one unit before being preempted by the second process. That, in turn, is preempted by the third process which is also preempted by the fourth process. After the longest process is done, the others get executed.
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
Cache memory is an extremely fast memory type that acts as a buffer between RAM and the CPU. It holds frequently requested data and instructions so that they are immediately available to the CPU when needed
### Diff between direct mapping and associative mapping & set associative mapping
Cache Mapping:

The process /technique of bringing data of main memory blocks into the cache block is known as cache mapping.
The mapping techniques can be classified as :
Direct Mapping
Associative
Set-Associative
1. Direct Mapping: Each block from main memory has only one possible place in the cache organization in this technique. 
For example : every block i of the main memory can be mapped to block j of the cache using the formula : 

j = i modulo m
Where : i = main memory block number
       j = cache block number
       m = number of blocks in the cache
The address here is divided into 3 fields : Tag, Block & Word.

To map the memory address to cache: The BLOCK field of the address is used to access the cache’s BLOCK. Then, the tag bits in the address is compared with the tag of the block. For a match, a cache hit occurs as the required word is found in the cache. Otherwise, a cache miss occurs and the required word has to be brought into the cache from the Main Memory. The word is now stored in the cache together with the new tag (old tag is replaced).

Example: If we have a fully associative mapped cache of 8 KB size with block size = 128 bytes and say, the size of main memory is = 64 KB. (Assuming word size = 1 byte) Then :

Number of bits for the physical address = 16 bits (as memory size = 64 KB = 26 × 210 = 216)
Number of bits for WORD = 7 bits (as block size = 128 bytes = 27)
No of Index bits = 13 bits (as cache size = 8 KB = 23 × 210 = 213)
No of BLOCK bits = Number of Index bits- Number of bits for WORD = 13 – 7 = 6bits

                                                                    OR
(No of cache Blocks = Cache size/block size = 8 KB / 128 Bytes = 8×1024 Bytes/128 Bytes = 26 blocks → 6bits)
No of TAG bits = Number of bits for the physical address — Number of bits in Index = 16-13 = 3 bits

2. Associative Mapping: Here the mapping of the main memory block can be done with any of the cache block. The memory address has only 2 fields here: word & tag. This technique is called as fully associative cache mapping.

Example: If we have a fully associative mapped cache of 8 KB size with block size = 128 bytes and say, the size of main memory is = 64 KB.  Then:

Number of bits for the physical address = 16 bits (as memory size = 64 KB = 26 × 210 = 216)
Number of bits in block offset = 7 bits (as block size = 128 bytes = 27)
No of tag bits = Number of bits for the physical address – Number of bits in block offset = 16-7 = 9 bits
No of cache Blocks = Cache size/block size = 8 KB / 128 Bytes = 8×1024 Bytes/128 Bytes = 26 blocks.

3. Set – Associative Mapping: It is the combination of advantages of both direct & associative mapping. 
Here, the cache consists of a number sets, each of which consists of a number of blocks. The relationships are :

n = w * L
i = j modulo w
where
i : cache set number
j : main memory block number
n : number of blocks in the cache
w : number of sets
L : number of lines in each set
This is referred to as L-way set-associative mapping. Block Bj can be translated into any of the blocks in set j using this mapping.

To map the memory address to cache: Using set field in the memory address, we access the particular set of the cache. Then, the  tag bits in the address are compared with the tag of all L blocks within that set.  For a match, a cache hit occur as the required word is found in the cache. Otherwise,  a cache miss occurs and the required word has to be brought in the cache from the Main Memory. According to the replacement policy used, a replacement is done if the cache is full.

Example: If we have a fully associative mapped cache of 8 KB size with block size = 128 bytes and say, the size of main memory is = 64 KB, and we have “2-way” set-associative mapping (Assume each word has 8 bits).   Then :

Number of bits for the physical address = 16 bits (as memory size = 64 KB = 26 * 210 = 216)
No of cache Blocks = Cache size/block size = 8 KB / 128 Bytes = 8×1024 Bytes/128 Bytes = 26 cache blocks.
No of Main Memory Blocks = MM size/block size = 64 KB / 128 Bytes = 64×1024 Bytes/128 Bytes = 29 MM blocks.
No of sets of size 2 = No of Cache Blocks/ L = 26/2 = 25 cache sets.(L = 2 as it is 2-way set associative mapping)
### Diff between multitasking and multiprocessing 
Multi-tasking : 
Multi-tasking is the logical extension of multiprogramming. In this system, the CPU executes multiple jobs by switching among them typically using a small time quantum, and these switches occur so frequently that the users can interact with each program while it is running. Multitasking is further classified into two categories: Single User & Multiuser. 
 Multiprocessing : 
Multiprocessing is a system that has two or more than two processors. In this, CPUs are added for increasing computing speed of the system. Because of Multiprocessing, there are many processes that are executed simultaneously. Multiprocessing is further classified into two categories: Symmetric Multiprocessing and Asymmetric Multiprocessing. 

