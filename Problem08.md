### Problem 8. Network Delay Time

You are given a network of `n` nodes, labeled from `1` to `n`.
You are also given `times`, a list of travel times as directed edges `times[i] = (u[i], v[i], w[i])`,
where `u[i]` is the source node, `v[i]` is the target node, and `w[i]` is the time it takes
for a signal to travel from source to target.

We will send a signal from a given node `k`.
Return _the minimum time it takes for all the `n` nodes to receive the signal_.
If it is impossible for all the n nodes to receive the signal, return `-1`.

Write your solution in [src/Problem08.java](src/Problem08.java)

<details>
<summary>Hint 1</summary>
We visit each node at some time, and if that time is better than the fastest time we've reached this node,
we travel along outgoing edges in sorted order.
Alternatively, we could use Dijkstra's algorithm.
</details>

#### Example 1:

<img width="217" height="239" alt="image" src="https://github.com/user-attachments/assets/3e3d3ab3-9c34-4ccd-9c8e-3e5f670d09f0" />

```
Input: times = [[2,1,1],[2,3,1],[3,4,1]], n = 4, k = 2
Output: 2
```

#### Example 2:

```
Input: times = [[1,2,1]], n = 2, k = 1
Output: 1
```

#### Example 3:

```
Input: times = [[1,2,1]], n = 2, k = 2
Output: -1
```

#### Constraints

+ `1 <= k <= n <= 100`
+ `1 <= times.length <= 6000`
+ `times[i].length == 3`
+ `1 <= u[i], v[i] <= n`
+ `u[i] != v[i]`
+ `0 <= w[i] <= 100`
+ All the pairs `(u[i], v[i])` are **unique**. (i.e., no multiple edges.)
