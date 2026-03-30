# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (445050174)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [16 march ]
**What I did**: Started working on the assignment

**Details**: Read the assignment instructions to understand what was required.
Downloaded the starter repository and opened the project files.
Changed the student ID in SchedulerSimulation.java to my real student ID.
Ran the program to see how the scheduler simulation works.

**Challenges**: At first it was a bit confusing to understand the structure of the code and how the processes and threads work together.


**Solution**: I spent some time reading the comments in the code and running the program to observe the output.

**Time spent**: 1 hour

---

### Entry 2 - [23 march]
**What I did**: Tried to understand the scheduling logic in the program

**Details**: Studied how the Process class works.
Observed how Thread.start() executes the process and how the scheduler waits using Thread.join().
Followed how processes move in and out of the ready queue.

**Challenges**: Understanding how the queue interacts with threads and how each process gets CPU time.

**Solution**: I followed the execution step by step and printed the output multiple times to understand the behavior

**Time spent**:  2 hour
---

### Entry 3 - [25 march]
**What I did**: Started implementing the first feature

**Details**: Added a priority field to the Process class.
Generated a random priority value for each process.
Updated the output to display the priority when the process enters the ready queue.

**Challenges**: Making sure the priority values were generated correctly and shown in the output.

**Solution**: Used the Random class to generate numbers between 1 and 5 and tested the program to confirm everything worked.

**Time spent**: 1 hour

---

### Entry 4 - [27 march]
**What I did**: Worked on the context switch feature

**Details**: Added a counter to track context switches.
Increased the counter whenever a new process started running.
Printed the total number of context switches at the end of the simulation.

**Challenges**: I had to think about where exactly to increment the counter in the code.

**Solution**:After reviewing the scheduler loop, I added the counter update before the thread execution.

**Time spent**: 2 hour

---

### Entry 5 - [29 march]
**What I did**: Implemented the waiting time tracking feature

**Details**: Added variables to track when a process enters the queue.
Used System.currentTimeMillis() to measure how long each process waits.
Calculated the waiting time and printed a summary table at the end.

**Challenges**: It was a bit tricky to calculate the waiting time correctly when processes were re-added to the queue

**Solution**: I adjusted the logic so the waiting time is updated every time the process returns to the queue.

**Time spent**: 1 hour 

---

### Entry 6 - [29 march]
**What I did**: Finalized the project and fixed GitHub issues

**Details**: I had some difficulty using GitHub because it was my first time working with it.At the beginning I did not understand how commits work or how to push my changes. Because the time was getting short, I rebuilt parts of the project again and organized the commits properly.

**Challenges**: Learning GitHub while also finishing the assignment was a bit stressful.

**Solution**: I reviewed the basic Git commands and tried committing changes step by step until everything worked correctly.

**Time spent**: 1 huor

---

## Summary

**Total time spent on assignment**: [8 hours]

**Most challenging part**: Understanding how the threads interact with the scheduler and learning how to properly use GitHub commits.

**Most interesting learning**: Seeing how Round-Robin scheduling works in practice and how multiple threads simulate CPU process execution.

**What I would do differently next time**: I would start earlier and practice using GitHub and commits before beginning the assignment
