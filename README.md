# Sudoku Solver

A fast and efficient **Sudoku solver** implemented in C++ using the **backtracking algorithm**.

## Description

This project solves Sudoku puzzles of any difficulty level. It uses a recursive backtracking approach to fill empty cells while validating against Sudoku rules (no duplicates in rows, columns, or 3×3 boxes).

## Algorithm

The solver employs the **Backtracking Algorithm**:

1. **Find Empty Cell**: Searches for the first empty cell (represented by 0) in the grid
2. **Try Numbers**: Attempts to place digits 1-9 in the empty cell
3. **Validate**: Uses `isSafe()` to check if the placement violates Sudoku rules
4. **Recurse**: If valid, recursively solves the remaining puzzle
5. **Backtrack**: If no solution is found, resets the cell and tries the next number

### Key Functions

- **`isSafe()`**: Validates if a number can be placed at a given position
  - Checks the row for duplicates
  - Checks the column for duplicates
  - Checks the 3×3 box for duplicates

- **`solveSudoku()`**: Recursively solves the puzzle using backtracking

- **`printBoard()`**: Displays the solved Sudoku grid

## Compilation and Execution

### Compile
```bash
g++ -o sudoku Sudoku.cpp
```

### Run
```bash
./sudoku
```

## Input Format

- Enter a 9×9 Sudoku grid
- Use **0** to represent **empty cells**
- Use **1-9** for given numbers
- Numbers should be space-separated or on separate lines

### Example Input
```
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9
```

## Output

The program outputs the solved Sudoku grid:
```
Solved Sudoku:
5 3 4 6 7 8 9 1 2
6 7 2 1 9 5 3 4 8
1 9 8 3 4 2 5 6 7
8 5 9 7 6 1 4 2 3
4 2 6 8 5 3 7 9 1
7 1 3 9 2 4 8 5 6
9 6 1 5 3 7 2 8 4
2 8 7 4 1 9 6 3 5
3 4 5 2 8 6 1 7 9
```

If no solution exists:
```
No solution exists
```

## Time Complexity

- **Best Case**: O(1) - When the puzzle is already solved
- **Average Case**: O(9^(n×m)) - Where n and m are rows and columns
- **Space Complexity**: O(1) for the recursion stack (bounded)

## Features

✅ Fast backtracking algorithm  
✅ Validates against all Sudoku rules  
✅ Handles multiple difficulty levels  
✅ Returns solution or reports if no solution exists  
✅ Efficient 3×3 box validation  

## Requirements

- C++11 or later
- g++ or any standard C++ compiler

## Notes

- The solver uses `vector<vector<int>>` for dynamic memory allocation
- All cells must contain values between 0-9
- Empty cells must be represented by 0
- The algorithm guarantees finding a solution if one exists

## License

Open source