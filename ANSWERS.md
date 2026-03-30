# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
A process is an independent program that runs in its own memory space and uses its own system resources such as memory and files. Each process operates separately from other processes, which means communication between processes is usually slower and requires special mechanisms. A thread, however, is a smaller unit of execution that runs inside a process and shares the same memory and resources with other threads of that process.

Threads are generally lighter and faster to create compared to processes because they share memory instead of creating separate memory spaces. In this assignment, we used threads because the scheduler simulation runs many tasks that belong to the same program and need to share data structures such as the ready queue and process map. Using threads makes the simulation more efficient and easier to manage within a single Java application.

in the code , each simulated process is represented by a thread using the Runnable interface The scheduler creates a new Thread for each Process object and runs it using Thread.start(), which allows the scheduler to simulate CPU scheduling more efficiently than creating separate operating system processes.






[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

In Round-Robin scheduling, if a process does not finish its execution during its assigned time quantum, the CPU stops executing it and places it back at the end of the ready queue. This allows other processes to use the CPU before the same process gets another chance to run. The process will eventually run again when it reaches the front of the queue


[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:

 P1 executing quantum [3000ms]
 P1 completed quantum 3000ms │ Overall progress: [████░░░░░░░░░░] 40%
Remaining time: 4500ms
 P1 yields CPU for context switch
 P1 added to ready queue
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

In this example, process P1 started executing and used its full time quantum. However, it still had remaining execution time after the quantum finished. Because of that, the scheduler removed it from the CPU and added it again to the ready queue. Later, when its turn comes again, the scheduler will execute it for another time quantum until it finishes.
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]  The thread is in the New state when it is created using new Thread(process) but before the start() method is called.

2. **Runnable**: [When does P1 become Runnable?]  The thread enters the Runnable state after the scheduler calls Thread.start(). At this point, the thread is ready to run and waiting for the CPU to execute it.

3. **Running**: [When is P1 Running?]  The thread is in the Running state when the CPU begins executing the run() method of the Process class. During this time, the process runs for the specified time quantum.

4. **Waiting**: [When/why would P1 be Waiting?] The thread enters the Waiting state when Thread.sleep() is called inside the run() method to simulate execution time. During this time, the thread pauses temporarily before continuing execution.

5. **Terminated**: [When is P1 Terminated?]  The thread reaches the Terminated state when the run() method finishes and the process has completed all of its execution time.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

A web server receives requests from many users at the same time. Each request can be handled by a separate thread that processes the request and sends a response back to the user.

Why Round-Robin: Round-Robin scheduling ensures that each user request receives CPU time fairly. If one request takes a long time to process, it will not block other requests because the CPU will switch between threads. This improves system responsiveness and ensures that all users receive service without long delays.

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]
In multiplayer online games, the server must handle actions from many players at the same time such as movement, communication, and game events.

**Why Round-Robin works well here**: 

Round-Robin scheduling ensures that every player action is processed fairly and regularly. By switching between threads quickly using a time quantum, the server can update multiple players efficiently and maintain a smooth gaming experience.

[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. The difference between threads and processes and how threads share memory within a program.
2. How Round-Robin scheduling works using a time quantum and ready queue.
3. How a thread lifecycle progresses from creation to termination during execution.

**Concepts I need to study more:**
1. Advanced thread synchronization techniques.
2. More complex CPU scheduling algorithms such as priority scheduling.
