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
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [Sunday, March 22, 2026, 4:00 PM]
**What I did**: Forked the repository and set up the project environment.

**Details**: 
- Created a GitHub account using my university email (@std.psau.edu.sa).
- Forked the starter repository from the instructor's page.
- Renamed the repository to OS-Assignment1-Abdulrhman-Alqahtani.

**Challenges**: I couldn't see the documentation files (.md) in VS Code initially.

**Solution**: I realized I opened only the Java file; I had to use "Open Folder" to see the entire repository structure.
**Time spent**: 1 hour.

---

### Entry 2 - [Monday, March 23, 2026, 11:30 AM]
**What I did**: Personalized the simulation with my Student ID.

**Details**: 
- Modified line 92 in SchedulerSimulation.java to set studentID = 443050700.
- Verified that the random seed correctly generates unique parameters for my simulation.
- Made my first commit to GitHub with the message "Set my student ID: 443050700".

**Challenges**: None for this specific task.

**Solution**: N/A.

**Time spent**: 30 minutes.

---

### Entry 3 - [Tuesday, March 24, 2026, 2:00 PM]
**What I did**: Implemented Feature 1 (Priority) and Feature 2 (Context Switch Counter).

**Details**: 
- Added the priority field to the Process class and updated the constructor.
- Created a static variable totalContextSwitches in the main class.
- Integrated the counter into the scheduler loop to track every time a process yields or finishes.

**Challenges**: Deciding the exact location to increment the context switch counter so it doesn't double-count.

**Solution**: I placed the increment logic specifically when a process is re-queued or when the last process runs to completion.

**Time spent**: 2 hours.

---

### Entry 4 - [Wednesday, March 25, 2026, 5:00 PM]
**What I did**: Implemented Feature 3 (Waiting Time Tracking) and UI enhancements.

**Details**: 
- Added logic to capture the creation time using System.currentTimeMillis().
- Calculated the total waiting time for each process once it finishes its execution.
- Enhanced the terminal output with ANSI colors to make the priority and context switches stand out.

**Challenges**: Formatting the final summary table to align correctly in the terminal.

**Solution**: Used String.format() to ensure columns are clean and readable for the instructor.

**Time spent**: 1.5 hours.

---

### Entry 5 - [Thursday, March 26, 2026, 4:30 AM]
**What I did**: Final documentation and video recording preparation.

**Details**: 
- Completed ANSWERS.md and REFLECTION.md with detailed technical explanations.
- Recorded a 3-minute video showing the code walkthrough and the unique simulation output.
- Uploaded the video to Google Drive and shared the link in README.md.

**Challenges**: Understanding the concept of "yielding" to explain it clearly in the video.

**Solution**: Researched how the Round-Robin algorithm forces a process to give up the CPU when its quantum expires.

**Time spent**: 2 hours.

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [7 hours.]

**Most challenging part**: Managing the thread synchronization and accurately counting context switches during the transition between the last two processes.
**Most interesting learning**: Understanding how Java's Thread.join() works to coordinate between the main scheduler and individual process threads.

**What I would do differently next time**: Start using Git branches for each feature to keep the development process even more organized.
