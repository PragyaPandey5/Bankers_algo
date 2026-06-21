# Bankers_algo
A C++ implementation of the Banker's Algorithm used for deadlock avoidance in operating systems. The project determines whether a system is in a safe state by analyzing resource allocation, maximum resource requirements, and available resources. It calculates the Need Matrix and generates a safe execution sequence for processes.
# Banker's Algorithm

## Overview

This project implements the **Banker's Algorithm**, a deadlock avoidance algorithm used in operating systems to allocate resources safely among multiple processes. The algorithm checks whether granting a resource request will leave the system in a safe state.

## Features

* Calculates the Need Matrix
* Determines if the system is in a safe state
* Generates a Safe Sequence (if one exists)
* Handles resource allocation requests
* Prevents deadlocks through safe resource management

## Concepts Used

* Deadlock Avoidance
* Resource Allocation
* Safe State Detection
* Need Matrix Calculation
* Operating System Scheduling Concepts

## Algorithm

The Banker's Algorithm works by:

1. Calculating the **Need Matrix**:

   ```
   Need = Maximum Resources - Allocated Resources
   ```

2. Finding a process whose resource needs can be satisfied with the available resources.

3. Simulating resource allocation and release.

4. Repeating the process until all processes can execute safely.

5. If all processes finish successfully, the system is in a **safe state**.

## Input

* Number of processes
* Number of resource types
* Allocation Matrix
* Maximum Requirement Matrix
* Available Resources Vector

## Output

* Safe Sequence (if available)
* Safe/Unsafe State indication

## Example

### Input

Allocation Matrix:

```
0 1 0
2 0 0
3 0 2
2 1 1
0 0 2
```

Maximum Matrix:

```
7 5 3
3 2 2
9 0 2
2 2 2
4 3 3
```

Available Resources:

```
3 3 2
```

### Output

```
System is in a Safe State.
Safe Sequence:
P1 → P3 → P4 → P0 → P2
```

## Technologies Used

* C++
* Standard Template Library (STL)

## Learning Outcomes

Through this project, I gained practical experience with:

* Operating System concepts
* Deadlock prevention techniques
* Resource allocation strategies
* Matrix-based problem solving
* C++ programming

## How to Run

### Compile

```bash
g++ bankers_algorithm.cpp -o banker
```

### Execute

```bash
./banker
```

## Project Structure

```
Bankers-Algorithm/
│
├── bankers_algorithm.cpp
├── README.md
└── sample_input.txt
```

## Author

Pragya Pandey
