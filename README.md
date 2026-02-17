# A* Algorithm Visualizer

An interactive Python visualization of the A* pathfinding algorithm using Pygame. Set a start and end point, draw obstacles, and watch the algorithm find the shortest path in real time.

[Demo Video](https://drive.google.com/file/d/1jeO9-d592tiUocJS4CRpuZ9QukkQyddC/view?usp=sharing)

## How It Works

A* is an optimized version of Dijkstra's Algorithm designed for single-destination pathfinding. It uses a heuristic (Manhattan distance) to prioritize paths that lead closer to the goal, making it the standard algorithm for navigation applications.

Each cell has three scores:
- **g_score** — actual cost from start to current node
- **h_score** — heuristic estimate to goal: `|x1 - x2| + |y1 - y2|`
- **f_score** — total estimated cost: `g + h`

The algorithm always expands the node with the lowest f_score, ensuring an optimal path.

## Controls

| Input | Action |
|-------|--------|
| Left Click (1st) | Place start point (orange) |
| Left Click (2nd) | Place end point (red) |
| Left Click (after) | Draw barriers (black) |
| Right Click | Erase a cell |
| Spacebar | Run the algorithm |
| C | Clear the grid |

## Color Legend

| Color | Meaning |
|-------|---------|
| White | Empty / unvisited |
| Orange | Start point |
| Red | End point |
| Black | Barrier |
| Green | Open set (being evaluated) |
| Blue | Closed set (already evaluated) |
| Yellow | Shortest path found |

## Requirements

- Python 3.x
- Pygame

## Installation & Usage

```sh
pip install pygame
python aStar.py
```

Opens an 800x800 window with a 50x50 interactive grid.

## Screenshot

<img width="1334" alt="A* Visualizer" src="https://user-images.githubusercontent.com/42263217/204078318-fcc6cdd1-021b-48b0-a5fe-4c135ce67ff0.png">
