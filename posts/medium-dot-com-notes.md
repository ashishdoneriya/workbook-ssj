---
title : "My medium.com website notes"
created : "2021-02-07T15:00:00+05:30"
updated : "2021-02-07T15:00:00+05:30"
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
