# Graphs - DFS - Easy Exercise

Practice problem to validate the Graphs - DFS pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Search Tree](binary-search-tree.md) | [Exercises Index](index.md) | [Graphs - BFS](graphs-bfs.md) |

## Pattern Reference

- [Graphs - DFS](../patterns/graphs-dfs.md)

## Problem

[Flood Fill](https://leetcode.com/problems/flood-fill/) — Difficulty: Easy

## Statement

An image is represented by an `m x n` integer grid `image` where `image[i][j]` represents the pixel value of the image.

You are also given three integers `sr`, `sc`, and `color`. You should perform a **flood fill** on the image starting from the pixel `image[sr][sc]`.

To perform a flood fill, consider the starting pixel, plus any pixels connected 4-directionally to the starting pixel of the same color as the starting pixel, plus any pixels connected 4-directionally to those pixels (also with the same color), and so on. Replace the color of all of the aforementioned pixels with `color`.

Return the modified image after performing the flood fill.

## Examples

```
image = [[1,1,1],[1,1,0],[1,0,1]], sr = 1, sc = 1, color = 2
-> [[2,2,2],[2,2,0],[2,0,1]]
image = [[0,0,0],[0,0,0]], sr = 0, sc = 0, color = 0
-> [[0,0,0],[0,0,0]]
```

## Constraints

- `m == image.length`, `n == image[i].length`
- `1 <= m, n <= 50`
- `0 <= image[i][j], color < 2^16`
- `0 <= sr < m`, `0 <= sc < n`

## What This Validates

- DFS on a grid with 4-directional movement.
- Tracking visited cells (or stopping recursion when the color changes).

## Hint

<details>
<summary>Hint</summary>

Save the starting color. Recurse into the four neighbors (up, down, left, right). Stop when a neighbor is out of bounds, already painted, or has a different color than the starting pixel.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Visits each reachable cell exactly once.
- [ ] Identified the time and space complexity.
- [ ] Explained the approach out loud.