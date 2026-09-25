# Binary Search - Easy Exercise

Practice problem to validate the Binary Search pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Heap / Priority Queue](heap-priority-queue.md) | [Exercises Index](index.md) | [Backtracking](backtracking.md) |

## Pattern Reference

- [Binary Search](../patterns/binary-search.md)

## Problem

[First Bad Version](https://leetcode.com/problems/first-bad-version/) — Difficulty: Easy

## Statement

You are a product manager and currently leading a team to develop a new product. Unfortunately, the latest version of your product fails the quality check. Since each version is developed based on the previous version, all the versions after a bad version are also bad.

Suppose you have `n` versions `[1, 2, ..., n]` and you want to find out the first bad one, which causes all the following ones to be bad.

You are given an API `isBadVersion(version)` which returns whether `version` is bad. Implement a function to find the first bad version. You should minimize the number of calls to the API.

## Examples

```
n = 5, bad = 4 -> 4
n = 1, bad = 1 -> 1
```

## Constraints

- `1 <= bad <= n <= 2^31 - 1`

## What This Validates

- Binary search on a monotonic sequence: `false, false, ..., true, true`.
- Finding the first index where a condition flips to `true`.

## Hint

<details>
<summary>Hint</summary>

The sequence of `isBadVersion` is monotonic. Use `low` and `high` pointers. When the middle version is bad, move `high` to `mid` (it may be the first bad one). When it is good, move `low` to `mid + 1`. Stop when `low` equals `high`.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Uses `O(log n)` calls to the API.
- [ ] Avoids infinite loops with the `low`/`high` update rule.
- [ ] Explained the approach out loud.