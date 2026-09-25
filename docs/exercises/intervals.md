# Intervals - Easy Exercise

Practice problem to validate the Intervals pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Trie](trie.md) | [Exercises Index](index.md) | [Monotonic Stack](monotonic-stack.md) |

## Pattern Reference

- [Intervals](../patterns/intervals.md)

## Problem

[Summary Ranges](https://leetcode.com/problems/summary-ranges/) — Difficulty: Easy

## Statement

You are given a **sorted unique** integer array `nums`.

Return the smallest sorted list of ranges that **cover all the numbers in the array exactly**. That is, each element of `nums` is covered by exactly one of the ranges, and there is no integer `x` such that `x` is in one of the ranges but not in `nums`.

Each range `[a,b]` in the list should be output as:

- `"a->b"` if `a != b`
- `"a"` if `a == b`

## Examples

```
nums = [0,1,2,4,5,7] -> ["0->2","4->5","7"]
nums = [0,2,3,4,6,8,9] -> ["0","2->4","6","8->9"]
```

## Constraints

- `0 <= nums.length <= 20`
- `-2^31 <= nums[i] <= 2^31 - 1`
- All the values of `nums` are unique.
- `nums` is sorted in ascending order.

## What This Validates

- Grouping consecutive elements into ranges.
- Handling the edge cases of single-element ranges and the empty array.

## Hint

<details>
<summary>Hint</summary>

Scan with a start pointer. While the next number is exactly one greater than the current one, keep extending the range. When the run breaks, close the range as `"start->end"` or `"start"` and open a new one.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Correctly formats single and multi-element ranges.
- [ ] Handles the empty array.
- [ ] Explained the approach out loud.