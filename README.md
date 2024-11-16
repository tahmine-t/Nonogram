# Nonogram
Nonogram Puzzle Solver - AI Course Project

This repository contains the implementation of a Nonogram puzzle solver using constraint satisfaction problem (CSP) techniques, based on the requirements of an AI course project. The project involves modeling the puzzle as a CSP, implementing algorithms such as Backtracking with Forward Checking, Minimum Remaining Values (MRV), and Least Constraining Value (LCV), and optimizing the solution using the AC-3 algorithm.

---

## **Project Overview**

### **Puzzle Description**  
The Nonogram puzzle is a logic puzzle where you are given an `n x n` grid. Initially, the grid is empty, and the objective is to fill it in such a way that all constraints are satisfied. The constraints are provided in the form of numbers indicating how many consecutive filled cells there should be in each row and column. 

For example, if a row has the constraint `1 2 2`, this means there should be:
- One filled cell,
- A gap,
- Two consecutive filled cells,
- Another gap, and
- Two consecutive filled cells.

### **Constraint Satisfaction Problem (CSP) Modeling**  
The Nonogram puzzle is modeled as a CSP:
- **Variables**: All cells of the grid (e.g., `n^2` variables for an `n x n` grid).
- **Domain**: Each variable can be in one of two states: filled (black cell) or empty (crossed cell).
- **Constraints**: The constraints provided in the puzzle specify the required sequences of consecutive filled cells for each row and column.

### **Solving Approach**  
The solution is achieved using:
1. **Backtracking with Forward Checking**: The main algorithm to search for a solution.
2. **Minimum Remaining Values (MRV)**: A heuristic to choose the variable with the fewest legal values remaining.
3. **Least Constraining Value (LCV)**: A heuristic to choose the value that leaves the most options for the remaining variables.
4. **AC-3 Algorithm**: Used to reduce the domain of the variables and ensure consistency across constraints.

---

## **Algorithms and Techniques Implemented**

- **Backtracking with Forward Checking**: Used to explore possible assignments and check consistency at each step.
- **Minimum Remaining Values (MRV)**: Heuristic to prioritize the most constrained variables.
- **Least Constraining Value (LCV)**: Heuristic to choose the value that maximizes the remaining options for other variables.
- **AC-3 Algorithm**: Arc consistency algorithm to propagate constraints and reduce domains, ensuring early detection of infeasible assignments.

---

## **Results and Evaluation**

After implementing the solver, the performance and correctness of the algorithms were evaluated on several Nonogram puzzles. The impact of the AC-3 algorithm was particularly notable, improving the speed and efficiency of the solver by reducing the search space early on.
