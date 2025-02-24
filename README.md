# Sudoku Solver

This is a Python implementation of a Sudoku solver that solves a given Sudoku puzzle using backtracking. The solution leverages constraint validation to check if a number can be placed in a particular cell based on the rules of Sudoku. 

## How It Works

The program works by:

1. **Finding the empty cells**: The board is iterated to locate an empty cell, represented by `0`.
2. **Checking if a guess is valid**: For each empty cell, it attempts to place numbers (1-9) and checks if the number can fit in the row, column, and the 3x3 square without violating Sudoku rules.
3. **Backtracking**: If placing a number leads to a valid solution, it proceeds to solve the next empty cell. If it encounters an invalid solution, it backtracks and tries a different number.
4. **Solving the puzzle**: The process repeats until the entire board is filled or it determines that the puzzle is unsolvable.

## Requirements

- Python 3.x

## How to Run

1. Clone this repository to your local machine:
    ```
    git clone https://github.com/FihriSina/sudoku-solver.git
    cd sudoku-solver
    ```

2. To solve a puzzle, you can modify the `puzzle` list in `solver.py` and run the program:
    ```bash
    python solver.py
    ```

3. The program will print the initial puzzle and the solved version if possible, or notify you if the puzzle is unsolvable.

## Example

For the following puzzle:

```
puzzle = [
  [0, 0, 2, 0, 0, 8, 0, 0, 0],
  [0, 0, 0, 0, 0, 3, 7, 6, 2],
  [4, 3, 0, 0, 0, 0, 8, 0, 0],
  [0, 5, 0, 0, 3, 0, 0, 9, 0],
  [0, 4, 0, 0, 0, 0, 0, 2, 6],
  [0, 0, 0, 4, 6, 7, 0, 0, 0],
  [0, 8, 6, 7, 0, 4, 0, 0, 0],
  [0, 0, 0, 5, 1, 9, 0, 0, 8],
  [1, 7, 0, 0, 0, 6, 0, 0, 5]
]
```

The program will attempt to solve it and output the solution:

```
Puzzle to solve:
* * 2 * * 8 * * *
* * * * * 3 7 6 2
4 3 * * * * 8 * *
* 5 * * 3 * * 9 *
* 4 * * * * * 2 6
* * * 4 6 7 * * *
* 8 6 7 * 4 * * *
* * * 5 1 9 * * 8
1 7 * * * 6 * * 5

Solved puzzle:
3 1 2 9 4 8 5 7 6 
8 9 5 6 7 3 7 6 2 
4 3 7 2 8 5 8 1 9 
7 5 8 1 3 2 4 9 6 
9 4 1 3 2 6 8 2 6 
5 6 3 4 6 7 2 8 1 
6 8 4 7 5 9 1 2 3
3 2 9 5 1 4 6 7 8 
1 7 6 8 9 6 3 3 5
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

1. Fork the repository.
2. Create a branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

```
