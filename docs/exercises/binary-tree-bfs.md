# Binary Tree - BFS - Easy Exercise

Practice problem to validate the Binary Tree - BFS pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Tree - DFS](binary-tree-dfs.md) | [Exercises Index](index.md) | [Binary Search Tree](binary-search-tree.md) |

## Pattern Reference

- [Binary Tree - BFS](../patterns/binary-tree-bfs.md)

## Problem

[Average of Levels in Binary Tree](https://leetcode.com/problems/average-of-levels-in-binary-tree/) — Difficulty: Easy

## Statement

Given the `root` of a binary tree, return the **average value** of the nodes on each level in the form of an array. Answers within `10^-5` of the actual answer will be accepted.

## Examples

```
root = [3,9,20,null,null,15,7] -> [3.00000,14.50000,11.00000]
root = [3,9,20,15,7]           -> [3.00000,14.50000,11.00000]
```

## Constraints

- The number of nodes in the tree is in the range `[1, 10^4]`.
- `-2^31 <= Node.val <= 2^31 - 1`

## What This Validates

- BFS level-by-level processing with a queue.
- Grouping nodes of the same level before moving to the next.

## Hint

<details>
<summary>Hint</summary>

Before processing each level, capture how many nodes are currently in the queue. That number is the size of the level. Process exactly that many nodes, summing their values, then divide by the level size.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Uses a queue and processes level by level.
- [ ] Handles nodes with values near the integer limits.
- [ ] Explained the approach out loud.