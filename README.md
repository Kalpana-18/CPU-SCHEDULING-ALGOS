# CPU-SCHEDULING-ALGOS
This repository contains implementations of various CPU scheduling algorithms in C++. The included algorithms are:

First Come First Serve (FCFS)
Round Robin (RR) with varying time quantum
Shortest Process Next (SPN)
Shortest Remaining Time (SRT)
Highest Response Ratio Next (HRRN)
Feedback (FB)
Feedback with varying time quantum (FBV)
Aging
Table of Contents
Overview
Algorithms
First Come First Serve (FCFS)
Round Robin with varying time quantum (RR)
Shortest Process Next (SPN)
Shortest Remaining Time (SRT)
Highest Response Ratio Next (HRRN)
Feedback (FB)
Feedback with varying time quantum (FBV)
Aging
Installation
Input Format
Contributors
Algorithms
First Come First Serve (FCFS)
The First Come First Serve (FCFS) algorithm executes processes in the order they arrive. It is straightforward but can lead to inefficiencies if a long process is ahead of shorter ones. FCFS does not prioritize any process and is considered non-preemptive, meaning that once a process starts, it runs to completion.

Round Robin with varying time quantum (RR)
Round Robin (RR) allocates CPU time slices (quanta) to processes in a cyclic order. In this implementation, the quantum is variable and can be adjusted per process requirements. This adaptability helps optimize CPU usage by allocating shorter quanta to shorter tasks and longer quanta to longer tasks, thus balancing the load and preventing starvation.

Shortest Process Next (SPN)
The Shortest Process Next (SPN) algorithm selects the process with the smallest burst time for execution. It is non-preemptive, meaning once a process starts, it will run until it either finishes or waits. SPN aims to reduce average waiting time by favoring shorter tasks, but it can lead to longer tasks being delayed.

Shortest Remaining Time (SRT)
Shortest Remaining Time (SRT) is a preemptive version of SPN. The algorithm continuously re-evaluates the processes in the queue and selects the one with the shortest remaining time for execution. This preemption allows it to adapt to new arrivals dynamically, optimizing average waiting time even when burst times are unknown beforehand.

Highest Response Ratio Next (HRRN)
Highest Response Ratio Next (HRRN) selects processes based on their response ratio, which is the ratio of waiting time to burst time. The process with the highest ratio is chosen next. HRRN is non-preemptive and aims to balance waiting time and burst time to optimize overall performance.

Feedback (FB)
The Feedback (FB) algorithm uses multiple queues with different priority levels to manage processes. Higher priority queues are processed first, and processes move between queues based on their execution time. This multi-level feedback system ensures that short and high-priority processes get more attention while longer processes eventually receive CPU time.

Feedback with varying time quantum (FBV)
Similar to FB, Feedback with varying time quantum (FBV) also uses multiple queues but assigns different time quanta to each level. This variance allows more efficient handling of processes by allocating appropriate CPU time based on their priority and requirements.

Aging
To counteract starvation, the Aging algorithm increments the priority of waiting processes over time. Each process starts with an initial priority, and the scheduler periodically increases the priority of all waiting processes. This ensures that even low-priority processes eventually get executed, preventing them from being starved by higher-priority ones.
