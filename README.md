# Sudoku Solver

A C++ implementation of a Sudoku puzzle solver using the **backtracking algorithm**. This program takes an unsolved Sudoku puzzle as input and finds the solution if one exists.

## Features

- ✅ Solves any valid 9x9 Sudoku puzzle
- ✅ Uses efficient backtracking algorithm
- ✅ Validates each number placement against Sudoku rules
- ✅ Interactive user input for puzzle entry
- ✅ Formatted output display

## How It Works

The solver uses a **backtracking** approach with three validation functions:

### 1. **isSafe() Function**
Validates if placing a number at a specific position is legal by checking:
- **Row**: No duplicate number in the same row
- **Column**: No duplicate number in the same column
- **3x3 Box**: No duplicate number in the same 3x3 grid

### 2. **solveSudoku() Function**
Implements the backtracking algorithm:
- Finds the first empty cell (value 0)
- Tries numbers 1-9 in that cell
- Recursively attempts to solve the remaining puzzle
- If a solution leads to a dead end, backtracks and tries the next number
- Returns `true` when the puzzle is completely solved

### 3. **printBoard() Function**
Displays the solved Sudoku grid in a readable format

## Compilation & Execution

### Compile:
```bash
g++ -o sudoku Sudoku.cpp
```

### Run:
```bash
./sudoku
```

## Usage

1. Run the program
2. Enter the Sudoku grid row by row
3. Use `0` to represent empty cells
4. The program will output the solved puzzle or indicate no solution exists

### Example Input:
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

### Example Output:
```
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

## Algorithm Complexity

- **Time Complexity**: O(9^(n×m)) in the worst case, where n×m is the number of empty cells
  - Average cases are much faster due to pruning
- **Space Complexity**: O(n×m) for recursion stack

## Requirements

- C++11 or later
- Standard C++ library (`bits/stdc++.h`)

## License

This project is open source and available under the MIT License.