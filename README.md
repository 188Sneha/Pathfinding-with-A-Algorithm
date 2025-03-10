# A* Pathfinding Algorithm

This project implements the A* (A-star) pathfinding algorithm to find the shortest path between a start and a goal node in a grid-based environment, considering obstacles.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [How it Works](#how-it-works)
- [Example](#example)
- [License](#license)

## Introduction

The A* algorithm is widely used for finding the shortest path in many fields such as game development, robotics, and navigation. It works by combining:
- **g(n)**: the cost from the start node to the current node.
- **h(n)**: the estimated cost from the current node to the goal (heuristic).

The algorithm calculates `f(n) = g(n) + h(n)` for each node and explores the node with the lowest `f(n)` value, ensuring the most efficient path is found.

## Usage

1. To run the algorithm, simply execute the Python script containing the implementation of A*.

2. Modify the grid or the start and goal points in the script to test different scenarios.

## How it Works

1. **Initialization**: The open list (nodes to be evaluated) and closed list (nodes already evaluated) are set up. The starting node is added to the open list with a cost of 0.
   
2. **Main Loop**: The algorithm repeatedly picks the node with the lowest `f(n)` value from the open list and evaluates its neighbors. The `f(n)` is calculated using the formula `f(n) = g(n) + h(n)`, where:
   - `g(n)` is the cost to get to the current node from the start.
   - `h(n)` is an estimate of the cost from the current node to the goal (heuristic).
   
3. **Path Reconstruction**: Once the goal node is reached, the path is reconstructed by following parent pointers from the goal back to the start.

4. **Termination**: The algorithm stops when it finds the goal node or when there are no more nodes to evaluate (if no path exists).

## Example

This algorithm can be tested with a variety of grid configurations. You can define your grid with obstacles (e.g., `1` for obstacles and `0` for free spaces), and specify start and goal points. The algorithm will calculate the shortest path from the start to the goal.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
