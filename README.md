# 8-Puzzle Solver

A Java implementation of an **A* search algorithm** to solve the N-by-N sliding puzzle (commonly called the 8-puzzle). The solver uses the **Manhattan priority function** and handles unsolvable puzzles efficiently.

---

## Features

- Represents the puzzle as a `Board` object with:
  - Board dimension
  - Hamming distance
  - Manhattan distance
  - Neighboring boards
  - Twin boards for solvability checks
- Uses **A\*** algorithm with **priority queue** (`MinPQ`) to find the shortest solution path.
- Detects unsolvable boards automatically.
- Returns:
  - Minimum number of moves to solve
  - Sequence of boards leading to the solution
- Optimized with **cached Manhattan priorities** for faster comparisons.

---

## Requirements

- Java 8 or higher
- [Princeton Algorithms library](https://algs4.cs.princeton.edu/code/)  

---

## Input Format

- Input file should contain the board dimension `N` followed by the `N-by-N` tile configuration.
- Blank space is represented by `0`.
Example for 3x3 puzzle:

3
8 1 3
4 0 2
7 6 5


---

## Usage

1. **Compile the code**:

```bash
javac Board.java Solver.java
Run the solver:

java Solver puzzle01.txt
Output includes:

Whether the puzzle is solvable

Minimum number of moves

Sequence of boards from initial state to goal

Example output:

Minimum number of moves = 4
 1  2  3 
 4  5  6 
 7  0  8 

 1  2  3 
 4  0  6 
 7  5  8 

 1  0  3 
 4  2  6 
 7  5  8 

 0  1  3 
 4  2  6 
 7  5  8 

 1  2  3 
 4  5  6 
 7  8  0 
If unsolvable:

No solution possible

