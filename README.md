# Bidirectional A* Solver for the N-Puzzle Problem

- The code is implemented using Bidirectional A Search* algorithm to solve the N-Puzzle problem.
- The goal is to reach a specific configuration by sliding tiles one at a time into blank space.
- The code first generates the random N*N matrix, then it calculate the solution path, and evaluates solution quality, cost and efficiency.
- Bidirectional A Search *:- Uses Manhattan distance as a heuristic for efficient bidirection searching, which is faster than unidirectional A* in larger puzzels.

## Code Description
- manhattan_distance(state, goal_flat): Computes the Manhattan distance between the current state and goal state, which serves as the heuristic for A*.
- get_neighbors(state): Generates neighboring states by simulating tile movements into the blank position.
- bidirectional_a_star(start, goal): Implements the bidirectional A* search algorithm.
    Expands nodes simultaneously from both the start and goal states.
    Checks if paths from both directions intersect, in which case a solution path is reconstructed.

## Performance Evaluation

The following table summarizes the performance of the Bidirectional A* algorithm on different puzzle sizes.

| Puzzle Size | Cost (Nodes Evaluated) | Quality (Moves) | Efficiency (Quality/Cost) | Time Taken (s) |
|-------------|------------------------|-----------------|---------------------------|----------------|
| 2x2         | 2             | 4   | 2          | 0.0sec     |
| 3x3         | 25             | 29   | 1.1600          | 0.1sec     |
| 4x4         | 51             | 53   | 1.0392          | 5.7sec     |


- **Puzzle Size**: The size of the puzzle grid (e.g., 2x2, 3x3, etc.).
- **Cost (Nodes Evaluated)**: The total number of nodes evaluated during the search. (Total noded evaluted during the search)
- **Quality (Moves)**: The number of moves in the solution path (or the number of steps to reach the goal).
- **Efficiency (Quality/Cost)**: A metric of the algorithm's efficiency, calculated as the ratio of Quality to Cost.
- **Time Taken (s)**: The time (in seconds) it took to run the Bidirectional A* search for the given puzzle size.

## Notes
- The N-Puzzle has complex branching and memory requirements, especially for larger dimenesions.
- Bidirectional A* significantly reduces the search space but may require significant memory as puzzle dimension increases.

