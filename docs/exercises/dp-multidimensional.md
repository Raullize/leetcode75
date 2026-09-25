# DP - Multidimensional - Easy Exercise

Practice problem to validate the DP - Multidimensional pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [DP - 1D](dp-1d.md) | [Exercises Index](index.md) | [Bit Manipulation](bit-manipulation.md) |

## Pattern Reference

- [DP - Multidimensional](../patterns/dp-multidimensional.md)

## Problem

[Pascal's Triangle](https://leetcode.com/problems/pascals-triangle/) — Difficulty: Easy

## Statement

Given an integer `numRows`, return the first `numRows` of Pascal's triangle.

In Pascal's triangle, each number is the sum of the two numbers directly above it.

## Examples

```
numRows = 5 -> [[1],[1,1],[1,2,1],[1,3,3,1],[1,4,6,4,1]]
numRows = 1 -> [[1]]
```

## Constraints

- `1 <= numRows <= 30`

## What This Validates

- Building a 2D table where each cell depends on previous cells.
- The recurrence `dp[i][j] = dp[i-1][j-1] + dp[i-1][j]` with edge handling.

## Hint

<details>
<summary>Hint</summary>

Each row starts and ends with `1`. For the middle cells of row `i`, the value is the sum of two adjacent cells from row `i - 1`.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Correctly handles the edges of each row.
- [ ] Identified the time and space complexity.
- [ ] Explained the approach out loud.