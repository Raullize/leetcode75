# Binary Search Tree - Easy Exercise

Practice problem to validate the Binary Search Tree pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Tree - BFS](binary-tree-bfs.md) | [Exercises Index](index.md) | [Graphs - DFS](graphs-dfs.md) |

## Pattern Reference

- [Binary Search Tree](../patterns/binary-search-tree.md)

## Problem

[Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/) — Difficulty: Easy

## Statement

Given a binary search tree (BST), find the lowest common ancestor (LCA) node of two given nodes in the BST.

The lowest common ancestor is defined between two nodes `p` and `q` as the lowest node in `T` that has both `p` and `q` as descendants (where we allow **a node to be a descendant of itself**).

## Examples

```
root = [6,2,8,0,4,7,9,null,null,3,5], p = 2, q = 8 -> 6
root = [6,2,8,0,4,7,9,null,null,3,5], p = 2, q = 4 -> 2
```

## Constraints

- The number of nodes in the tree is in the range `[2, 10^5]`.
- `-10^9 <= Node.val <= 10^9`
- All `Node.val` are **unique**.
- `p != q`
- `p` and `q` will exist in the BST.

## What This Validates

- Exploiting the BST property (`left < node < right`) to prune the search space.
- Deciding which subtree to descend into based on the values of `p` and `q`.

## Hint

<details>
<summary>Hint</summary>

If both `p` and `q` are smaller than the current node, the LCA must be in the left subtree. If both are larger, it is in the right subtree. Otherwise, the current node splits them and is the LCA.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Uses the BST ordering property, not a generic tree search.
- [ ] Identified the complexity for a balanced tree.
- [ ] Explained the approach out loud.