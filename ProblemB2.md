### Problem B2. Find If Path Exists

There is a **bi-directional** graph with `n` vertices, where each vertex is labeled from `0` to `n-1` (**inclusive**).
The edges in the graph are represented as a 2D integer array `edges`, where each `edges[i] = {u, v}` denotes a bi-directional edge between vertex `u` and vertex `v`.
Every vertex pair is connected by **at most one** edge, and no vertex has an edge to itself.

You want to determine if there is a **valid path** that exists from vertex `source` to vertex `destination`.

Given edges and the integers `n`, `source`, and `destination`, return `true` if there is a valid path from `source` to `destination`, or `false` otherwise.

Write your solution in [src/ProblemB2.java](src/ProblemB2.java)

#### Example 1:

<img width="141" height="121" alt="image" src="https://github.com/user-attachments/assets/e87420f6-20d6-484b-a7b0-b05efb2d986d" />

```
Input: n = 3, edges = [[0,1],[1,2],[2,0]], source = 0, destination = 2
Output: true

Explanation:
There are two paths from vertex 0 to vertex 2:
0 -> 1 -> 2
0 -> 2
```
#### Example 2:

<img width="281" height="141" alt="image" src="https://github.com/user-attachments/assets/d0ee8603-d936-4c67-9c65-e80b7e680f70" />

```
Input: n = 6, edges = [[0,1],[0,2],[3,5],[5,4],[4,3]], source = 0, destination = 5
Output: false
Explanation: There is no path from vertex 0 to vertex 5.
```

#### Constraintes

```
1 <= n <= 200000
0 <= edges.length <= 200000
edges[i].length == 2
0 <= u, v <= n-1
u != v
0 <= source, destination <= n-1
There are no duplicate edges.
There are no self edges.
```
