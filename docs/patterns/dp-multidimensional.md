# DP - Multidimensional

Multidimensional DP appears when the state needs more than one variable.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [DP - 1D](dp-1d.md) | [Patterns Index](index.md) | [Bit Manipulation](bit-manipulation.md) |

## When to Use

- Grid problems.
- Sequences compared against each other.
- State with position and remaining resource.

## TypeScript Example

```ts
function uniquePaths(m: number, n: number): number {
  const dp: number[][] = Array.from({ length: m }, () => Array(n).fill(0));

  for (let i = 0; i < m; i++) dp[i][0] = 1;
  for (let j = 0; j < n; j++) dp[0][j] = 1;

  for (let i = 1; i < m; i++) {
    for (let j = 1; j < n; j++) {
      dp[i][j] = dp[i - 1][j] + dp[i][j - 1];
    }
  }

  return dp[m - 1][n - 1];
}
```

## Key Idea

Think of a table where each cell represents a state of the problem.

## Complexity

- Time: `O(mn)`.
- Space: `O(mn)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=dynamic+programming+2d+leetcode
