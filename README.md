# NuSMV 3 philosophers and 2 forks
Dining Philosophers Problem — 3 Philosophers, 2 Forks

A NuSMV MODEL CHECKING EXERCISE

This repository contains a formal model and verification tasks for a variant of the classic Dining Philosophers Problem, implemented in NuSMV.
Unlike the traditional version (where the number of forks equals the number of philosophers), this model considers 3 philosophers and only 2 forks, introducing additional synchronization challenges.

PROBLEM DESCRIPTION
Three philosophers (P0, P1, P2) alternate between thinking, getting hungry, and eating.
To eat, a philosopher must obtain both forks. However, in this simplified model the two forks are treated as a single shared resource: they are either both free or both occupied.

This constraint makes it impossible for more than one philosopher to eat at the same time and introduces possible issues such as:
Mutual exclusion
Starvation
Deadlock
Scheduling fairness

To avoid uncontrolled concurrency, the system uses a turn-based scheduler.
The turn variable ensures that only one philosopher at a time is allowed to change state, preventing random interleavings and allowing predictable verification.
