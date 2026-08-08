# DP - 1D

1D DP solves problems where the state depends on one main dimension.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Backtracking](backtracking.md) | [Patterns Index](index.md) | [DP - Multidimensional](dp-multidimensional.md) |

## When to Use

- Stairs.
- Maximum sum in a sequence.
- Optimization on a linear array.

## TypeScript Example

```ts
function climbStairs(n: number): number {
  if (n <= 2) return n;

  let prev2 = 1;
  let prev1 = 2;

  for (let i = 3; i <= n; i++) {
    const current = prev1 + prev2;
    prev2 = prev1;
    prev1 = current;
  }

  return prev1;
}
```

## Key Idea

Clearly define the state, transition, and base case.

## Complexity

- Time: `O(n)`.
- Space: `O(1)` when storage is optimized.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=dynamic+programming+1d+leetcode
