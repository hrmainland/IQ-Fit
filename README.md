# IQ Fit Solver

A Python implementation that solves the IQ Fit puzzle game using depth-first search algorithm with backtracking.

## Overview

IQ Fit is a puzzle game where players must fit 10 colored pieces onto a 5x10 grid board. Each piece has two different forms and can be rotated in 4 directions (0°, 90°, 180°, 270°). This solver finds valid solutions by systematically trying all possible piece placements.

## Features

- **Depth-First Search Algorithm**: Uses recursive backtracking to explore all possible piece configurations
- **Piece Rotation**: Supports all 4 rotational orientations for each piece form
- **Visual Display**: Matplotlib-based grid visualization showing the solved puzzle
- **Flexible Constraints**: Supports pre-placed pieces for specific puzzle challenges

## Game Pieces

The solver includes 10 unique pieces, each with two alternative forms:

- Dark Blue (DB)
- Green (GR) 
- Dark Green (DG)
- Yellow (YE)
- Light Blue (LB)
- Purple (PU)
- Orange (OR)
- Blue (BL)
- Red (RE)
- Pink (PI)

## Files

- `solve.py` - Standalone Python script with the core solving algorithm
- `solve.ipynb` - Jupyter notebook with visualization capabilities using matplotlib

## Usage

### Python Script
```bash
python solve.py
```

### Jupyter Notebook
Open `solve.ipynb` in Jupyter and run the cells to see the visual solution.

## Algorithm

The solver uses a recursive depth-first search approach:

1. Take a piece from the remaining pieces list
2. Try both forms of the piece
3. Test all 4 rotations for each form
4. For each rotation, try all valid positions on the board
5. If a placement works, recursively solve for remaining pieces
6. If no solution is found, backtrack and try the next configuration
7. Return the first complete solution found

## Requirements

- Python 3.x
- matplotlib (for visualization in Jupyter notebook)
- numpy (for visualization in Jupyter notebook)

## Board Representation

- 5x10 grid (5 rows, 10 columns)
- Empty spaces represented as `None`
- Filled spaces contain the piece's color code (e.g., "DB", "GR")
- Solution ensures no empty spaces remain on the board