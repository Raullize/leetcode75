# Monotonic Stack - Easy Exercise

Practice problem to validate the Monotonic Stack pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Intervals](intervals.md) | [Exercises Index](index.md) | [README](../../README.md) |

## Pattern Reference

- [Monotonic Stack](../patterns/monotonic-stack.md)

## Problem

[Next Greater Element I](https://leetcode.com/problems/next-greater-element-i/) — Difficulty: Easy

## Statement

The **next greater element** of some element `x` in an array is the first greater element that is **to the right** of `x` in the same array.

You are given two **distinct 0-indexed** integer arrays `nums1` and `nums2`, where `nums1` is a subset of `nums2`.

For each `0 <= i < nums1.length`, find the index `j` such that `nums1[i] == nums2[j]` and determine the next greater element of `nums2[j]` in `nums2`. If there is no next greater element, then the answer for this query is `-1`.

Return an array `ans` of length `nums1.length` such that `ans[i]` is the next greater element as described above.

## Examples

```
nums1 = [4,1,2], nums2 = [1,3,4,2] -> [-1,3,-1]
nums1 = [2,4],   nums2 = [1,2,3,4] -> [3,-1]
```

## Constraints

- `1 <= nums1.length <= nums2.length <= 1000`
- `0 <= nums1[i], nums2[i] <= 10^4`
- All integers in `nums1` and `nums2` are unique.
- All the integers of `nums1` also appear in `nums2`.

## What This Validates

- The monotonic stack: finding the next greater element for every position in `nums2` in one pass.
- Combining a hash map (to look up positions in `nums1`) with the stack.

## Hint

<details>
<summary>Hint</summary>

Scan `nums2` from left to right. Keep a stack of indices whose next greater element is still unknown. When the current value is greater than the value at the top of the stack, pop and record the current value as the answer for that index. Store the results in a map, then build the answer for `nums1`.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Avoids the naive `O(n^2)` per-element scan.
- [ ] Each element enters and leaves the stack at most once.
- [ ] Explained the approach out loud.