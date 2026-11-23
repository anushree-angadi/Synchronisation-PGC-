# Experiment: Analyze Synchronization Mechanisms in Parallel Programs

## Objective
To implement and study synchronization mechanisms in shared-memory parallel programs and compare their correctness, execution time, and scalability.

## Synchronization Mechanisms Implemented
- Race Condition (No Synchronization)
- Critical Section
- Atomic Operation
- Barrier
- Semaphore
- OpenMP Lock

## Technologies Used
- C Programming
- Ubuntu 24.04 LTS
- GCC Compiler
- OpenMP
- POSIX Threads (Pthreads)
- Semaphore Library
- VMware

## Programs
| Program | Description |
|---|---|
| `race.c` | Demonstrates race conditions without synchronization |
| `critical.c` | Uses critical sections to protect shared data |
| `atomic.c` | Uses atomic operations for safe counter updates |
| `barrier.c` | Synchronizes threads at a barrier |
| `semaphore.c` | Uses semaphores for mutual exclusion |
| `compare_sync.c` | Compares synchronization methods with different thread counts |

## Experiment Parameters
- Shared counter increments: 10,000,000
- Thread counts tested: 1, 2, 4, and 8
- Synchronization methods compared: None, Critical, Atomic, and Lock

## Results

### Individual Programs
- Race condition program executed successfully.
- Critical section produced the correct counter.
- Atomic operation produced the correct counter.
- Barrier synchronized threads before and after the barrier.
- Semaphore program produced the correct counter value.

### Comparison Experiment
The synchronization mechanisms were compared using different thread counts.

| Mechanism | Correctness | Performance |
|---|---|---|
| None | Incorrect with multiple threads | Fastest, but unreliable |
| Critical | Correct | Slower due to waiting |
| Atomic | Correct | Fast and efficient |
| Lock | Correct | Slower due to lock contention |

## Conclusion
The experiment demonstrated the importance of synchronization in parallel programs. Without synchronization, race conditions lead to incorrect results. Critical sections, atomic operations, locks, and semaphores ensure correctness but introduce synchronization overhead. Atomic operations provide a good balance of correctness and performance for simple shared-variable updates.
