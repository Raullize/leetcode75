# Backtracking - Easy Exercise

Practice problem to validate the Backtracking pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Search](binary-search.md) | [Exercises Index](index.md) | [DP - 1D](dp-1d.md) |

## Pattern Reference

- [Backtracking](../patterns/backtracking.md)

## Problem

[Sum of All Subset XOR Totals](https://leetcode.com/problems/sum-of-all-subset-xor-totals/) — Difficulty: Easy

## Statement

The **XOR total** of an array is defined as the bitwise `XOR` of all its elements, or `0` if the array is **empty**.

- For example, the XOR total of the array `[2,5,6]` is `2 XOR 5 XOR 6 = 1`.

Given an array `nums`, return the sum of all XOR totals for every subset of `nums`.

Note: subsets with the same elements should be counted multiple times. An array `a` is a subset of an array `b` if `a` can be obtained from `b` by deleting some (possibly zero) elements of `b`.

## Examples

```
nums = [1,3]   -> 6   (0 + 1 + 3 + (1 XOR 3))
nums = [5,1,6] -> 28
nums = [3,4,5,6,7,8] -> 480
```

## Constraints

- `1 <= nums.length <= 12`
- `1 <= nums[i] <= 20`

## What This Validates

- Enumerating all subsets by choosing to include or skip each element.
- The "explore choices and undo them" mindset of Backtracking.

## Hint

<details>
<summary>Hint</summary>

Recurse over the array index. At each element, branch into two choices: include it in the XOR total or skip it. When you reach the end of the array, add the accumulated XOR to the sum.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Generates every subset exactly once.
- [ ] Understood why the number of subsets is `2^n`.
- [ ] Explained the approach out loud.