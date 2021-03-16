---
title : "My medium.com website notes"
created : "2021-02-07T15:00:00+05:30"
updated : "2021-03-09T15:00:00+05:30"
categories : ["software-engineering"]
tags : ["java"]
summary : "This page contains my medium.com notes"
---

### Norms to follow  
Architectural Decision Records

### [Handling Concurrent Requests in a RESTful](https://medium.com/swlh/handling-concurrent-requests-in-a-restful-api-5a25a4b81a1)  
By using Optimistic locking (checking existing version in database while updating).

### [Threads life cycle (thread states)](https://medium.com/javarevisited/java-concurrency-thread-life-cycle-4869432474b)
The java.lang.Thread class contains a static State enum — which defines its potential states. The thread can only be in one of these states at a time:
* **NEW** — a newly created thread that has not yet started the execution
* **RUNNABLE** — either running or ready for execution but it’s waiting for resource allocation
* **WAITING** — waiting for some other thread to perform a particular action without any time limit
* **TIMED_WAITING** — waiting for some other thread to perform a specific action for a specified period
* **BLOCKED** — waiting to acquire a lock to enter or re-enter a synchronized block/method
* **TERMINATED** — has completed its execution

### [Be Careful With Java Parallel Streams](https://levelup.gitconnected.com/be-careful-with-java-parallel-streams-3ed0fd70c3d0)
* Donot use parallelStream in LinkedList, BufferredReader etc.
* Java Streams use ForkJoinPool to launch parallel executions.

### [From Coding Bootcamp Graduate to Building Distributed Databases](https://medium.com/swlh/from-coding-bootcamp-graduate-to-building-distributed-databases-29acbb723d8)
* Learn Computer Fundamentals like DS & A, OS, Computer Architecture Networking.
* When using something, learn how it works, its internals also.
* The goal of these side projects is to condense years of experience and skills into the shortest amount of time.
* The side projects also serve as an opportunity to develop skill sets that you wish to acquire, but that you wouldn’t otherwise get to develop at your day job.
* Whatever niche you settle on, try and spend at least two years working on a meaty problem in that space. Spending at least two years on the same “problem” is important because it’s how you develop depth.

### [Steps to learn a new technology](https://betterprogramming.pub/my-4-step-strategy-to-learn-any-new-technology-quickly-c277299b35c)
* Learn fundamental concepts.
* Tutorials are a form of passive learning, which is inefficient. Taking tutorials might kill your interest because it can be boring to learn the syntax of a new language (e.g. "if you type this, you will see that…")
* Speeding through the tutorial.
* The goal is not to remember everything covered in the tutorial but rather to understand the concepts and know what the technology is capable of. You can easily look up the syntax later or review the tutorial while you practice.
* Don't be afraid to ditch the current tutorial and go for another one
* Build something, no matter how trivial.
* Give Interview for that technology.

### [How to Avoid Learning Mistakes](https://betterprogramming.pub/how-to-avoid-the-number-one-learning-mistake-a-lack-of-deliberate-practice-a17bff39eb70)
* Lack of Planning
* Do Regular Practice instead of one in a week
* Lack of Focus - Do not code while watching tutorial video. Close all unnecessary tabs. Leave your phone in other room. Donot copy and paste code.
