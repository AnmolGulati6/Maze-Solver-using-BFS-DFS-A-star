# Maze Solver

This project, done as part of the CS-540 Intro to AI course at UW Madison. This repository contains a Python project for solving mazes using various search algorithms. The project provides implementations for solving mazes using A*, Breadth-First Search (BFS), and Depth-First Search (DFS) algorithms.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Installation](#installation)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Maze Solver project is designed to solve mazes represented as a 2D grid. It includes implementations of popular search algorithms to find the shortest path between a given start position and an end position in the maze.

The following search algorithms are included:

- A* Algorithm (A_star)
- Breadth-First Search (BFS)
- Depth-First Search (DFS)

The project also provides utility functions for parsing maze data, generating maze visualizations, and calculating heuristics for search algorithms.

## Usage

To use this project, you need to provide a maze in text format and specify the start and end positions. The project offers several functions for different tasks:

- `q1(txt_maze: List[str]) -> str`: Returns the maze in its original text format.
- `q2(maze: MazeType) -> str`: Converts and returns the maze as a comma-separated string of move succession symbols.
- `q3(maze: MazeType, start_position: MazePosition, end_position: MazePosition) -> str`: Solves the maze using Depth-First Search (DFS) and returns the sequence of moves as a string.
- `q4(txt_maze: List[str], start_position: MazePosition, end_position: MazePosition) -> str`: Solves the maze using Depth-First Search (DFS) and updates the text maze to show the path.
- `q5(maze: MazeType, start_position: MazePosition, end_position: MazePosition) -> str`: Creates a matrix indicating visited positions during BFS traversal.
- `q6(maze: MazeType, start_position: MazePosition, end_position: MazePosition) -> str`: Creates a matrix indicating visited positions during DFS traversal.
- `q7(maze: MazeType, end_position: MazePosition) -> str`: Calculates and returns a matrix of Manhattan distances from each position to the end position.
- `q8(maze: MazeType, start_position: MazePosition, end_position: MazePosition) -> str`: Solves the maze using A* algorithm with Manhattan heuristic and updates the text maze to show the path.
- `q9(maze: MazeType, start_position: MazePosition, end_position: MazePosition) -> str`: Solves the maze using A* algorithm with Euclidean heuristic and updates the text maze to show the path.

To use these functions, call them with the appropriate arguments, and they will return the desired results.

## Installation

1. Clone this repository: `git clone https://github.com/your-username/maze-solver.git`
2. Navigate to the project directory: `cd maze-solver`

## Examples

Here are some examples of how to use the functions provided by this project:

```python
from maze_solver import *

# Load maze from file and parse it
txt_maze = get_maze('maze.txt')
parsed_maze = parse_maze(txt_maze)
start_position, end_position = find_starting_positions(parsed_maze)

# Example usage of functions
q1(txt_maze)
q2(parsed_maze)
q3(parsed_maze, start_position, end_position)
q4(txt_maze, start_position, end_position)
q5(parsed_maze, start_position, end_position)
q6(parsed_maze, start_position, end_position)
q7(parsed_maze, end_position)
q8(parsed_maze, start_position, end_position)
q9(parsed_maze, start_position, end_position)
```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
