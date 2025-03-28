Valid Path in an Undirected Graph

Problem Statement

You are given a bi-directional graph with n vertices, where each vertex is labeled from 0 to n - 1 (inclusive). The edges in the graph are represented as a 2D integer array edges, where each edges[i] = [u_i, v_i] denotes a bi-directional edge between vertex u_i and vertex v_i. Every vertex pair is connected by at most one edge, and no vertex has an edge to itself.

You need to determine if there exists a valid path from the given source vertex to the destination vertex.

Input Format

n (integer): Number of vertices in the graph.

edges (2D integer array): A list of edges where each edge connects two vertices.

source (integer): The starting vertex.

destination (integer): The target vertex.

Output Format

Return true if there exists a path from source to destination, otherwise return false.

Example

Input

n = 3
edges = [[0,1],[1,2],[2,0]]
source = 0
destination = 2

Output

true

Explanation

There are two possible paths from vertex 0 to vertex 2:

0 → 1 → 2

0 → 2
Since a valid path exists, the function returns true.

Constraints

1 <= n <= 10^5

0 <= edges.length <= 10^5

edges[i].length == 2

0 <= u_i, v_i < n

0 <= source, destination < n

No duplicate edges and no self-loops.

Approach

1. Graph Representation

Use an adjacency list (vector<vector<int>>) to store the graph.

Traverse the graph using Breadth-First Search (BFS) or Depth-First Search (DFS) to check for a path.

2. BFS Approach (Iterative)

Use a queue to explore nodes level by level.

Maintain a visited array to avoid revisiting nodes.

If we reach destination, return true.

If the queue is exhausted without finding destination, return false.

Implementation (BFS in C++)

Complexity Analysis

Graph Construction: O(n + m) (where m is the number of edges)

BFS Traversal: O(n + m)

Overall Complexity: O(n + m), which is efficient for large inputs.

Alternative Approach (DFS)

Instead of BFS, we can also use DFS (Depth-First Search) to explore paths recursively.

Summary

Graph Representation: Adjacency List

Traversal: BFS (or DFS alternative)

Time Complexity: O(n + m)

Space Complexity: O(n + m) (for adjacency list and visited array)

This solution efficiently determines whether a valid path exists between the given source and destination. 🚀

