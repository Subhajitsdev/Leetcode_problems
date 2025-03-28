# Valid Path in an Undirected Graph

## Problem Statement

You are given an **undirected graph** with `n` vertices, labeled from `0` to `n - 1`. The edges in the graph are represented as a **2D integer array** `edges`, where:

- Each `edges[i] = [ui, vi]` represents a **bi-directional** edge between vertex `ui` and vertex `vi`.
- Each vertex pair has **at most one edge**.
- No vertex has an edge to itself.

Your task is to determine whether there is a **valid path** that exists from a given `source` vertex to a `destination` vertex.

## Input Format

- An integer `n` representing the number of vertices.
- A list of edges `edges`, where `edges[i] = [ui, vi]` represents an undirected edge.
- An integer `source` representing the starting vertex.
- An integer `destination` representing the target vertex.

## Output Format

- Return `true` if there is a valid path from `source` to `destination`, otherwise return `false`.

## Example

### 📝 **Input**
```
n = 3
edges = [[0,1], [1,2], [2,0]]
source = 0
destination = 2
```
### ✅ **Output**
```
true
```
### 🔍 **Explanation**
```
There are two paths from vertex 0 to vertex 2:
- 0 → 1 → 2
- 0 → 2
```
### 💡 **Approach**
To determine if a valid path exists, we can use graph traversal techniques like:

🔹 #Breadth-First Search (BFS)
Uses a queue for level-wise traversal.

Ensures the shortest path is found first.

Suitable for unweighted graphs like this one.
