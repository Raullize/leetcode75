# Binary Tree - DFS - Easy Exercise

Practice problem to validate the Binary Tree - DFS pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Linked List](linked-list.md) | [Exercises Index](index.md) | [Binary Tree - BFS](binary-tree-bfs.md) |

## Pattern Reference

- [Binary Tree - DFS](../patterns/binary-tree-dfs.md)

## Problem

[Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/) — Difficulty: Easy

## Statement

Given the `root` of a binary tree, invert the tree, and return its root.

## Examples

```
root = [4,2,7,1,3,6,9] -> [4,7,2,9,6,3,1]
root = [2,1,3]         -> [2,3,1]
root = []              -> []
```

## Constraints

- The number of nodes in the tree is in the range `[0, 100]`.
- `-100 <= Node.val <= 100`

## What This Validates

- Recursive DFS: processing a node then recursing into children.
- Thinking about the base case (`null` root).

## Hint

<details>
<summary>Hint</summary>

At each node, swap its left and right children, then invert each child recursively. The base case is a `null` node, which returns `null`.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Uses recursion correctly with a clear base case.
- [ ] Identified the time and space complexity.
- [ ] Explained the approach out loud.