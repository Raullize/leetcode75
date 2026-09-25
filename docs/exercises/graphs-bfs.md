# Graphs - BFS - Easy Exercise

Practice problem to validate the Graphs - BFS pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Graphs - DFS](graphs-dfs.md) | [Exercises Index](index.md) | [Heap / Priority Queue](heap-priority-queue.md) |

## Pattern Reference

- [Graphs - BFS](../patterns/graphs-bfs.md)

## Problem

[Find if Path Exists in Graph](https://leetcode.com/problems/find-if-path-exists-in-graph/) — Difficulty: Easy

## Statement

There is a bi-directional graph with `n` vertices, where each vertex is labeled from `0` to `n - 1` (inclusive). The edges in the graph are represented as a 2D integer array `edges`, where each `edges[i] = [ui, vi]` denotes a bi-directional edge between vertex `ui` and vertex `vi`. Every vertex pair is connected by at most one edge, and no vertex has an edge to itself.

You want to determine if there is a valid path that exists from vertex `source` to vertex `destination`.

Return `true` if there is a valid path, or `false` otherwise.

## Examples

```
n = 3, edges = [[0,1],[1,2],[2,0]], source = 0, destination = 2 -> true
n = 6, edges = [[0,1],[0,2],[3,5],[5,4],[4,3]], source = 0, destination = 5 -> false
```

## Constraints

- `1 <= n <= 2 * 10^5`
- `0 <= edges.length <= 2 * 10^5`
- `edges[i].length == 2`
- `0 <= ui, vi <= n - 1`
- `ui != vi`
- `0 <= source, destination <= n - 1`

## What This Validates

- Building an adjacency list from an edge list.
- BFS traversal with a `visited` set to avoid infinite loops.

## Hint

<details>
<summary>Hint</summary>

Build an adjacency list, then start a BFS from `source`. Expand the queue one node at a time, marking each node as visited before adding its neighbors. If you ever dequeue `destination`, return `true`.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Builds the adjacency list correctly.
- [ ] Marks nodes as visited to avoid reprocessing.
- [ ] Identified the time and space complexity.