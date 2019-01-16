# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

### What is concurrency? What is parallelism? What's the difference?
> Concurrency is when a process divides its time between different tasks, giving the illusion of parallelism. Parallelism on the other hand is when two tasks run in parallel, both being executed separately.
 

### Why have machines become increasingly multicore in the past decade?
> Machines have become increasingly multicore because transistors can no longer be made any smaller, halting the increase in the speed of single-core processors.
 

### What kinds of problems motivates the need for concurrent execution?
> (Or phrased differently: What problems do concurrency help in solving?)
Concurrency helps solving user experience problems and server problems. If it weren't for concurrency, an user would not be able to have multiple programs open at the same time. Concurrency also allows for multiple connections being made to one server at the same time.
 

### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
> (Come back to this after you have worked on part 4 of this exercise)
Concurrency makes programming more complex, but at the same time, it allows developers to create applications and software which otherwise would be impossible.
 

### What are the differences between processes, threads, green threads, and coroutines?
> Processes are OS-managed and owns its own memory and threads. A thread can run on the CPU. Green threads are not OS-managed threads, but are scheduled by an 'ordinary' user-lever process, not by the kernel. A coroutine is simular to a thread, with its of stack, own local variables and its own instruction points, but it shares global variables and mostly anything else with other coroutines.
 

### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
> `pthread_create()` and `threading.Thread()` creates normal CPU threads. `go` created a coroutine.
 

### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
> GIL is a mutex, which prevents multiple Python threads from accessing the same resource at the same time. This implies that Python execution is limited to a single core.

### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
> The answer is starting Python threads on different cores.

### What does `func GOMAXPROCS(n int) int` change? 
> It changes the number of processor cores the GO code might use.
