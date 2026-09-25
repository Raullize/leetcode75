# Two Pointers - Easy Exercise

Practice problem to validate the Two Pointers pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Array / String](array-string.md) | [Exercises Index](index.md) | [Sliding Window](sliding-window.md) |

## Pattern Reference

- [Two Pointers](../patterns/two-pointers.md)

## Problem

[Move Zeroes](https://leetcode.com/problems/move-zeroes/) — Difficulty: Easy

## Statement

Given an integer array `nums`, move all `0`s to the end of it while maintaining the relative order of the non-zero elements.

You must do this **in-place** without making a copy of the array.

## Examples

```
nums = [0,1,0,3,12]  -> [1,3,12,0,0]
nums = [0]           -> [0]
```

## Constraints

- `1 <= nums.length <= 10^4`
- `-2^31 <= nums[i] <= 2^31 - 1`

## What This Validates

- The "read and write pointers" variation of Two Pointers.
- Mutating the input in a single pass without extra space.

## Hint

<details>
<summary>Hint</summary>

Use a slow pointer that marks where the next non-zero value should be written, and a fast pointer that scans for non-zero values. When the fast pointer finds a non-zero value, write it to the slow position and advance both.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Uses `O(1)` extra space (in-place).
- [ ] Runs in a single `O(n)` pass.
- [ ] Explained the approach out loud.