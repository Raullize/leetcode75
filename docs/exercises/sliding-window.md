# Sliding Window - Easy Exercise

Practice problem to validate the Sliding Window pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Two Pointers](two-pointers.md) | [Exercises Index](index.md) | [Prefix Sum](prefix-sum.md) |

## Pattern Reference

- [Sliding Window](../patterns/sliding-window.md)

## Problem

[Contains Duplicate II](https://leetcode.com/problems/contains-duplicate-ii/) — Difficulty: Easy

## Statement

Given an integer array `nums` and an integer `k`, return `true` if there are two **distinct indices** `i` and `j` in the array such that `nums[i] == nums[j]` and `abs(i - j) <= k`.

## Examples

```
nums = [1,2,3,1], k = 3    -> true
nums = [1,0,1,1], k = 1    -> true
nums = [1,2,3,1,2,3], k = 2 -> false
```

## Constraints

- `1 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`
- `0 <= k <= 10^5`

## What This Validates

- Keeping a window of the last `k` elements as you scan.
- The fixed-size / bounded-window variation of Sliding Window.

## Hint

<details>
<summary>Hint</summary>

As you move the right end of the window, add the new value to a set. When the window grows beyond `k` elements, remove the value that just left the window. If a value is already in the set, you found your answer.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Achieves `O(n)` time, not `O(n * k)`.
- [ ] Correctly evicts elements that fall outside the window.
- [ ] Explained the approach out loud.