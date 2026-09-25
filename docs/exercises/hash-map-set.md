# Hash Map / Set - Easy Exercise

Practice problem to validate the Hash Map / Set pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Prefix Sum](prefix-sum.md) | [Exercises Index](index.md) | [Stack](stack.md) |

## Pattern Reference

- [Hash Map / Set](../patterns/hash-map-set.md)

## Problem

[Contains Duplicate](https://leetcode.com/problems/contains-duplicate/) — Difficulty: Easy

## Statement

Given an integer array `nums`, return `true` if any value appears **at least twice** in the array, and return `false` if every element is distinct.

## Examples

```
nums = [1,2,3,1]  -> true
nums = [1,2,3,4]  -> false
nums = [1,1,1,3,3,4,3,2,4,2] -> true
```

## Constraints

- `1 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

## What This Validates

- Using a `Set` for fast existence checks and deduplication.
- Recognizing when a hash-based structure replaces an `O(n^2)` scan.

## Hint

<details>
<summary>Hint</summary>

Add each number to a `Set` as you scan. If you try to add a number that is already present, you have a duplicate.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Achieves `O(n)` time.
- [ ] Identified the extra space used by the set.
- [ ] Explained the approach out loud.