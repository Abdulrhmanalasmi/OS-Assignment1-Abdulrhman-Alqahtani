# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

A process is an independent program execution environment that has its own complete set of private resources and memory space, making it heavy to create and manage. On the other hand, a thread exists within a process and shares the same memory and resources with other threads, which makes it much more "lightweight" and efficient for multitasking. In this assignment, we used threads because they allow our simulation to manage multiple tasks (P1, P2, etc.) simultaneously within a single Java application without the high overhead of creating separate OS-level processes. This shared memory model is perfect for our processQueue where all threads need to access and update the same data structures quickly.

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

In Round Robin scheduling, if a process cannot finish its total burst time within the fixed time quantum, it must yield the CPU to ensure fairness for other waiting tasks. Once the time quantum expires, the process is moved from the "Running" state back to the end of the "Ready Queue" to wait for its next turn. This ensures that no single process can hog the CPU resources for too long, providing responsive performance for all active processes in the system.

Example from my output:
In this snippet from my output (Seed: 443050700), P1 ran for its 2000ms quantum but still had 50% of its work remaining. Because it wasn't finished, it triggered the "yield" message and was re-added to the back of the queue, allowing the next process to start its execution.

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

Tracking the lifecycle of process P1 in my simulation shows how it moves through different JVM thread states based on the scheduler's logic:

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: P1 is in the New state when the Thread object is first instantiated inside the addProcessToQueue method before any execution begins.

2. **Runnable**: It becomes Runnable the moment it is added to the processQueue, meaning it is ready and waiting for the CPU to pick it up.

3. **Running**: P1 enters the Running state when the scheduler calls currentThread.start(), and it begins executing its logic inside the run() method.
4. **Waiting**: During execution, P1 enters a timed Waiting state when Thread.sleep() is called to simulate the passage of time for each quantum step.

5. **Terminated**: Finally, P1 reaches the Terminated state after its remainingTime hits zero and the main thread calls join() to confirm its completion.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Servers (e.g., Apache or Nginx)

**Description**: 
Web servers handle thousands of simultaneous requests from different users at the same time.

**Why Round-Robin works well here**: It ensures that every user gets a small slice of CPU time to process their request. This prevents one user downloading a massive file from blocking other users who just want to load a simple text page, maintaining high responsiveness.

### Example 2: PC Operating System GUI

**Description**: 
Modern operating systems like Windows or macOS run many background apps (music, browser, antivirus) while the user interacts with the desktop.

**Why Round-Robin works well here**: Round-Robin scheduling with threads allows the OS to switch rapidly between these apps, giving each one a "turn" so quickly that the user perceives them as running perfectly in parallel.


---

## Summary

**Key concepts I understood through these questions:**
1. The efficiency of using Threads over Processes for resource sharing.
2. How Round-Robin ensures fairness through Time Quantums and yielding.
3. The specific transitions a thread makes from creation to termination (Lifecycle).

**Concepts I need to study more:**
1. Advanced synchronization techniques between threads to prevent data races.
2. How different OS kernels implement multi-level feedback queues.
