# Prefix Sum - Easy Exercise

Practice problem to validate the Prefix Sum pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Sliding Window](sliding-window.md) | [Exercises Index](index.md) | [Hash Map / Set](hash-map-set.md) |

## Pattern Reference

- [Prefix Sum](../patterns/prefix-sum.md)

## Problem

[Find Pivot Index](https://leetcode.com/problems/find-pivot-index/) — Difficulty: Easy

## Statement

Given an array of integers `nums`, calculate the **pivot index** of this array.

The pivot index is the index where the sum of all the numbers strictly to the left of the index is equal to the sum of all the numbers strictly to the index's right.

If the index is on the left edge of the array, then the left sum is `0` because there are no elements to the left. This also applies to the right edge of the array.

Return the **leftmost** pivot index. If no such index exists, return `-1`.

## Examples

```
nums = [1,7,3,6,5,6]  -> 3
nums = [1,2,3]        -> -1
nums = [2,1,-1]       -> 0
```

## Constraints

- `1 <= nums.length <= 10^4`
- `-1000 <= nums[i] <= 1000`

## What This Validates

- Using prefix sums to answer subarray range queries in `O(1)`.
- Turning a "sum to the left / sum to the right" problem into a formula.

## Hint

<details>
<summary>Hint</summary>

Compute the total sum once. For each index, the left sum can be accumulated as you go, and the right sum is `total - leftSum - nums[i]`. Compare them directly without building a second prefix array.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Achieves `O(n)` time.
- [ ] Uses `O(1)` extra space (no prefix array needed here).
- [ ] Explained the approach out loud.