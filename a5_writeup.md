# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. How do the performance and efficiency of the Depth-First Search (DFS) and Breadth-First Search (BFS) algorithms compare when solving Sudoku puzzles? In what scenarios might one approach be preferable over the other?
The depth first search is more efficent for solving sudoku puzzles.  This is because of how sudoku puzzles are strucctured, they have more depth than they have breath so it is more efficient to use a depth search rather than a breath first search.  The ability for DFS to quickly backtrack is also helpful.


2. How did the choice of data structures (like the Stack for DFS and Queue for BFS) impact the implementation and functionality of the algorithms? Are there alternative data structures or design patterns that could have been used to achieve the same objectives?
The use of data structuers like stacks for DFS was useful because LIFO let us put the current possible state or states of the cell onto the list and pop them off as soon as we needed to.   You could use a regular list for this same task instead of a stack but you would have to specificy what element of the list you were removing every time.  This results in not only more work but also introduces more room for error.


3. Considering the current implementation, how might the Sudoku solver be adapted or extended for larger puzzles or different types of grid-based logic games? How can the lessons learned from this assignment be applied to real-world problem-solving or optimization challenges?
The way that the current sudoku solver fucntions could allow for it to be modiified to work in other grid based puzzle games.  In some cases it may be easier to have a similar structure to some elements of the sudoku solver rather than a exact copy or modified version.  You might be able to adapt this to program to play minesweeper.  Its not exactly suited for it with its focous on 3x3 grids but the principle is similar overall.  It would be able to use its ability to determine the cells around it and then determine the most or least likely place that a mine would be in.   