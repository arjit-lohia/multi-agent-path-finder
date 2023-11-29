<div align="center">
<img src="images/path.png" alt="Mult Agent Path FInding.png" width="1500"/>

# ⚡ Multi Agent Path Finding

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-orange)
![CBS](https://img.shields.io/badge/Conflict%20Based%20Searching-8A2BE2)
![A*](https://img.shields.io/badge/A*%20Algorithm-green)
</div>

&nbsp;

# Abstract
<div align = "justify">
<i>
The problem involves scheduling 'k' robots on a 2-D grid to minimize the overall completion time for 'k' shipment tasks. Each robot starts at a designated location, 
picks up a component, delivers it, and moves to a final destination. Obstacles on the grid must be navigated around. The objective is to optimize 
task assignments and travel paths to achieve the shortest total completion time.
</i>
</div>

# Getting Started

## Basic Idea:
```
1. Break the problem into three cases for finding the path:
    a. Start to Pick-up location
    b. Pick-up location to Drop Location
    c. Drop location to Destination
2. Utilize Low-Level Implementation of CBS to find the path of these three cases independently, by employing the A* algorithm
3. Follow this step to find the path of all 'k' agents
4. Finally, use the High-Level Implementation of CBS to resolve conflicting paths among 'k' agents
```

## Solution Steps
### 1. Initialization:
> a. Define the dimension of the shop floor, the number of robots, obstacles, starting points, pick-up points, drop locations, and final destinations.

> b. Specify all constraints, such as the boundary of the floor, conflict constraints, and obstacles that robots should consider while finding an optimal path. Ensure that no two agents can occupy the same position (x, y) at time t.

> c. Define the cost function and the optimal heuristic. For instance, consider Euclidean distance as a heuristic.

### 2. Low-Level Search:
> a. Apply the A* Algorithm for each robot to compute optimal paths from start to goal, considering all defined constraints and heuristics.

### 3. High-Level Search:
> a. Define a validate function to check for conflicting states among all agents.

> b. Use the CBS algorithm to find non-conflicting paths by considering robot task assignments and resolving conflicts.

### 4. Execution:
> a. Utilize CBS in a stepwise manner. Initially, use it to find an optimal path from the starting point to the pick-up point, then find the optimal path from the pick-up point to the drop location, and finally from the drop location to the final destination.

# Example 


