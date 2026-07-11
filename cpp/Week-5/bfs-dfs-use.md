# Comparison between BFS and DFS with Usecase

Solution :
Traversal - BFS visits nodes level by level whereas DFS goes as deep as possible before backtracking.
Data Structure Used - BFS uses Queue (FIFO) whereas DFS uses Stack (LIFO) or Recursion.
Shortest Path - BFS finds shortest path (in an unweighted graph) whereas DFS never finds shortest path.
Memory Usage - Usually higher in BFS as compared to DFS.
Best Use - BFS is used for finding the nearest or shortest path whereas DFS is used for exploring all possible paths or deep structures.

# BFS (Breadth-First Search)
Usecase - Finding the shortest route in a metro system. BFS checks all nearby stations first and guarantees the route with the fewest stations (in an unweighted network)

# DFS (Depth-First Search)
Usecase - Searching for a file in nested folders. It explores one branch completely before checking other folders, making it a natural fit for hierarchical structures like file systems.