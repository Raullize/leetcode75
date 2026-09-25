# Linked List - Easy Exercise

Practice problem to validate the Linked List pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Queue](queue.md) | [Exercises Index](index.md) | [Binary Tree - DFS](binary-tree-dfs.md) |

## Pattern Reference

- [Linked List](../patterns/linked-list.md)

## Problem

[Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/) — Difficulty: Easy

## Statement

Given the `head` of a singly linked list, return the middle node of the linked list.

If there are two middle nodes, return the **second** middle node.

## Examples

```
head = [1,2,3,4,5]    -> node with value 3
head = [1,2,3,4,5,6]  -> node with value 4
```

## Constraints

- The number of nodes in the list is in the range `[1, 100]`.
- `1 <= Node.val <= 100`

## What This Validates

- The "pointers moving at different speeds" variation of Two Pointers applied to a linked list.
- Traversing a singly linked list without knowing its length.

## Hint

<details>
<summary>Hint</summary>

Move a slow pointer one step at a time and a fast pointer two steps at a time. When the fast pointer reaches the end, the slow pointer is at the middle. For an even number of nodes, this naturally lands on the second middle.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Uses only one pass and `O(1)` extra space.
- [ ] Returns the second middle node for even-length lists.
- [ ] Explained the approach out loud.