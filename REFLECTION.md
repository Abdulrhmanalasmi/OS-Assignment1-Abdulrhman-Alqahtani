# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[Through this assignment, I gained a deep understanding of how multithreading allows a single program to handle multiple tasks simultaneously by sharing CPU resources. I learned how to implement the Runnable interface and manage thread states like Running, Waiting, and Terminated using Java's built-in methods. It was fascinating to see how the Round-Robin algorithm ensures fairness by giving each thread a specific time quantum before forcing it to yield the CPU. I also understood the importance of thread coordination using join() to ensure the main simulation only finishes after all child threads have completed their work. This experience showed me that concurrency is not just about running things at the same time, but about managing their lifecycle and communication efficiently.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[The most challenging part was accurately implementing the Context Switch Counter and the Waiting Time tracking. It was difficult to determine the exact point in the code where the CPU officially switches from one process to another without double-counting the transitions. Additionally, calculating the waiting time required me to carefully track the difference between the initial creation time and the final completion time while accounting for the time spent executing. Understanding the "yield" logic in the provided starter code also took some time, as I had to trace how threads move back to the ready queue. These challenges were directly related to the core OS concepts of scheduling and process management we studied in class.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[I overcame these challenges by using a systematic debugging approach and utilizing external learning resources. I spent a significant amount of time reading the official Java documentation on the Thread class and researching how Round-Robin scheduling is visualized in real-time. Using System.out.println() with ANSI colors helped me track the flow of execution in the terminal, which made it easier to see exactly when a context switch occurred. I also drafted my logic and technical answers in external notes to refine my understanding before implementing them in the final code. Furthermore, I used AI as a learning assistant to clarify complex concepts like "thread yielding" and to help me structure my documentation professionally.]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Multithreading is essential in modern software, such as Web Browsers, where one thread handles the user interface while others download images or execute scripts in the background. Another great example is in Video Games, where separate threads are used for physics calculations, audio processing, and rendering graphics to ensure a smooth player experience. In mobile apps, threads prevent the "freezing" of the screen by moving heavy data processing tasks away from the main UI thread. Understanding these concepts allows me to build applications that are more responsive, efficient, and capable of handling high loads of data. The principles I learned in this assignment, like time-slicing and resource sharing, are the same ones used by large-scale systems like Netflix or Google to serve millions of users.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
