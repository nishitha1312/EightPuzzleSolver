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

