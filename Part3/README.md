# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency means more than one program is being executed at the same time.Parallelism means one program is split into sub tasks and these are executed at the same time in parallel.Concurrency is about managing multiple programs execution either sequentially (one after other) or partially (portion of a program at a time).On the other hand parallel programs execution is about managing single program execution either completely (start to end) or splitting (sub tasks).During parallel execution there is no sharing of memory and not necessarily the machine also but during concurrent execution there is sharing of memory (operate on same data) and machine.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *Initially it was all about the clock speed that is increasing the frequency results in increased performance but a time came when it was not feasible to increase the frequency above 3 to 4 GHz because of heat production and leakage current.It became very difficult and expensive to cool down the heat produced during running at such high frequencies and researchers start thinking now what should be done to improve performance.At this phase the rate of increasing the clock frequency decreased and the rate of use of parallel computing increased which boost the concept of multi cores technology which results increased overall performance.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Your answer here*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Your answer here*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > *Your answer here*
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *Your answer here*
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *Your answer here*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *Your answer here*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *Your answer here*
