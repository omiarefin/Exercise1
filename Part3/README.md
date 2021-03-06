# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency means more than one program is being executed at the same time.Parallelism means one program is split into sub tasks and these are executed at the same time in parallel.Concurrency is about managing multiple programs execution either sequentially (one after other) or partially (portion of a program at a time).On the other hand parallel programs execution is about managing single program execution either completely (start to end) or splitting (sub tasks).During parallel execution there is no sharing of memory and not necessarily the machine also but during concurrent execution there is sharing of memory (operate on same data) and machine.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *Initially it was all about the clock speed that is increasing the frequency results in increased performance but a time came when it was not feasible to increase the frequency above 3 to 4 GHz because of heat production and leakage current.It became very difficult and expensive to cool down the heat produced during running at such high frequencies and researchers start thinking now what should be done to improve performance.At this phase the rate of increasing the clock frequency decreased and the rate of use of parallel computing increased which boost the concept of multi cores technology which resulted increased overall performance over the last decades.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *1.All problems cannot be solved by parallel algortihm and all machines does not support parallel computation in such cases concurrent programming might be very useful (some programs are well suited to solve with concurrency).
    2.Input/output intensive programs wait for the input or output operations to be completed but this waiting time can be used for another task if concurrent programming is used (reduce latency and redundancy).
    3.If the tasks does not have common sense of time its better to solve them with concurrent programming because any task can be executed with available resources at any time (difficulty in scheduling tasks at the right granularity onto the processors).
    4.Some programs spend a lot of time in memory allocations and garbage collections so in such cases its better to use concurrent programming for avoiding memory issues and save time that is increased performance.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *I think it makes a programmer's life harder because while doing concurrent programming he might need to consider low level things such as sharing of memory/data and message passing with addition tension of deadlocks and race conditions.*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Processes: OS managed,have own virtual address space,can be interrupted by the system,can run in parllel with other processes. Threads: OS managed,present inside a process,share the same virtual address,can be interrupted by the system,can be run in parallel with other threads.
Green threads: same as threads but not OS managed sharing same memory,cannot be interrupted by the system,cannot be run in parallel,can be multiplexed. Coroutines: same as threads but not OS managed,cannot be run in parallel,cannot be multiplexed*
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *pthread_create()*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *Global Interpreter Lock (GIL) prevents CPU based multiple threads to be executed in parallel in python which results in increased execution time but for I/O bound multiple threads its not a problem because the lock is shared among them when waiting for I/O.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *Multiple processes can be used instead of multiple threads where each process has its own python interpreter and memory address so GIL won't be a problem.The multiprocessing module of pyhton enables us to create multiple processes easily.*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *func GOMAXPROCS(n int) int changes the number of operating system threads that can execute user level go code simulataneously.*
