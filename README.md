# 🧵 OS Final Project — Priority Inversion Problem

This project simulates the **Priority Inversion Problem** in Operating Systems and provides a solution using **Priority Donation**. The goal is to understand how task scheduling and resource locking can lead to performance bottlenecks when priority levels are not properly managed.

---

## 🚩 Introduction

**Priority Inversion** occurs when a high-priority thread is waiting for a resource held by a lower-priority thread, but that lower-priority thread is continuously preempted by medium-priority threads. This project implements:

- A simulation of the problem.
- A multithreaded demonstration.
- A resolution using **priority donation**.
- An extended version supporting **multiple shared resources**.

---

## 🎯 Project Objectives

- Simulate priority inversion using 3 threads.
- Demonstrate the issue in a multithreaded environment.
- Resolve it using **priority inheritance**.
- Extend the solution to handle **nested resources**.

---

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Library:** `threading`
- **Operating System:** Windows

---

## 🔄 Implementation Breakdown

### ✅ Task 1: Simulate Priority Inversion
- **Threads**:
  - High-priority (H)
  - Medium-priority (M)
  - Low-priority (L)
- The low-priority thread holds a lock.
- High-priority thread waits for the lock.
- Medium-priority thread preempts the low-priority thread.
- Demonstrates blocking of high-priority thread — i.e., *priority inversion*.

### ✅ Task 2: Multithreaded Demonstration
- Converts Task 1 into a more explicit **thread-based** environment.
- Uses mutexes and schedulers.
- Behavior is similar but emphasizes real-world thread contention.

### ✅ Task 3: Resolve Using Priority Donation
- Implements **priority donation mechanism**:
  - High-priority thread temporarily donates its priority to the low-priority thread.
  - The low-priority thread finishes faster and releases the lock.
  - High-priority thread continues execution.

### ✅ Task 4: Multiple Resource Management
- Introduces two shared resources.
- Handles **nested locks**.
- Ensures deadlock prevention and efficient priority inheritance.

---

## 📌 Output Explanation (Summary)

### 🔹 Task 1 Output:
- High-priority thread blocked due to lock held by low-priority.
- Medium-priority thread runs in between — causing **priority inversion**.

### 🔹 Task 2 Output:
- Confirms the above behavior in multithreaded setup.

### 🔹 Task 3 Output:
- Priority donation allows low-priority thread to finish faster.
- High-priority thread resumes execution quickly — problem resolved.

### 🔹 Task 4 Output:
- Simulates multiple resources with locking/unlocking sequences.
- Ensures that **nested priority inheritance** works effectively.

---

## 📌 Key Takeaways

- Real-world systems like **Mars Pathfinder** have faced this issue.
- Priority inversion must be handled in **real-time systems**.
- **Priority inheritance/donation** is a proven solution to this OS-level challenge.

---

## 📌 Future Scope

- Implement **Priority Ceiling Protocol**.
- Test on **RTOS (Real-Time Operating Systems)**.
- Analyze performance using different **scheduling algorithms**.

---

## 👩‍💻 Author

- **Name:** Mehwish Nasir  
- **Course:** Operating Systems  
- **Project Title:** Priority Inversion Problem  
- **Department:** Data Science  
- **University:** University of Management & Technology

---

