# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**
From this assignment, I learned how multithreading works in Java and how multiple threads can share CPU time using scheduling algorithms like Round-Robin. I understood how to create threads using the Runnable interface and how each process is executed inside a thread using Thread.start(). I also learned about different thread states such as running, waiting, and terminated, especially when using Thread.sleep() and Thread.join(). One important concept I learned is how threads do not run truly at the same time, but instead switch quickly using context switching. Implementing the scheduler helped me understand how CPU time is divided fairly among processes. I also learned how to simulate real operating system behavior using simple Java code. Overall, this assignment gave me a practical understanding of how multithreading works beyond just theory.

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**
The most challenging part of this assignment was implementing the waiting time calculation correctly. Since processes are executed multiple times and re-enter the ready queue, it was difficult to track exactly how long each process was waiting. I had to understand when a process is actually waiting versus when it is running. Another challenge was updating the lastQueueEnter time correctly every time the process was re-added to the queue. At first, I tried to access the variable directly but faced errors due to private access. Also, making sure that the calculation using System.currentTimeMillis() was accurate required careful placement of the code. This part was challenging because it required a deeper understanding of timing and process states. It was not just coding, but also thinking logically about the execution flow.

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

To overcome these challenges, I broke the problem into smaller parts and focused on one feature at a time. I first added the necessary variables like creationTime, lastQueueEnter, and waitingTime to track the timing. Then I used a setter method to update lastQueueEnter whenever the process was added back to the queue. I also made sure to calculate waiting time at the beginning of the run() method using the current system time. When I faced errors, I carefully read the error messages and fixed issues like accessing private variables incorrectly. I tested the program multiple times to verify that the waiting time values were reasonable. Additionally, I made commits after each feature to isolate problems and avoid confusion. This step-by-step approach helped me solve the issues effectively.

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

Multithreading is widely used in many real-world applications. For example, web browsers use multiple threads to load web pages, play videos, and respond to user input at the same time. In this case, each task runs in a separate thread, which improves performance and responsiveness. Another example is in gaming, where threads are used to handle graphics rendering, user input, and background calculations simultaneously. In operating systems, CPU scheduling algorithms like Round-Robin are used to ensure fairness between running processes. The concepts I learned in this assignment, such as context switching and time quantum, directly apply to these systems. Multithreading helps make applications faster and more efficient by utilizing CPU resources properly. This assignment helped me understand how these concepts are applied in real-life systems.

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

I would like to learn more about advanced synchronization techniques such as mutexes, semaphores, and how to avoid race conditions. I am also interested in learning how multithreading works in real operating systems at a deeper level. Understanding how threads are managed internally by the OS would help me connect theory with real-world systems.

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

I would rate myself as Intermediate. I understand the basic concepts like thread creation, execution, and scheduling. I also have a good understanding of how Round-Robin works and how context switching happens. However, I still need more practice with advanced topics like synchronization and thread safety.

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

The assignment was very useful because it helped me understand multithreading through practical implementation. It was not easy, especially the waiting time feature, but it improved my problem-solving skills. The use of visual output made it easier to understand what is happening in the simulation. Overall, it was a good balance between theory and practical work.

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
