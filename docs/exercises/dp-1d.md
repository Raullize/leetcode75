# DP - 1D - Easy Exercise

Practice problem to validate the DP - 1D pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Backtracking](backtracking.md) | [Exercises Index](index.md) | [DP - Multidimensional](dp-multidimensional.md) |

## Pattern Reference

- [DP - 1D](../patterns/dp-1d.md)

## Problem

[Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/) — Difficulty: Easy

## Statement

You are given an integer array `cost` where `cost[i]` is the cost of `i`th step on a staircase. Once you pay the cost, you can either climb one or two steps.

You can either start from the step with index `0`, or the step with index `1`.

Return the minimum cost to reach the top of the floor.

## Examples

```
cost = [10,15,20] -> 15
cost = [1,100,1,1,1,100,1,1,100,1] -> 6
```

## Constraints

- `2 <= cost.length <= 1000`
- `0 <= cost[i] <= 999`

## What This Validates

- Defining a 1D state (`dp[i]` = min cost to reach step `i`).
- Writing the recurrence and the base cases.

## Hint

<details>
<summary>Hint</summary>

To reach step `i`, you came from step `i - 1` or step `i - 2`, so `dp[i] = cost[i] + min(dp[i - 1], dp[i - 2])`. The answer is `min(dp[n - 1], dp[n - 2])` because the top is beyond the last index. Can you keep only the last two values instead of a full array?

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Correctly defines the state, transition, and base cases.
- [ ] Achieves `O(n)` time and ideally `O(1)` space.
- [ ] Explained the approach out loud.