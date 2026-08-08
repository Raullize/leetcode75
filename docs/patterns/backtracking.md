# Backtracking

Backtracking builds solutions step by step and undoes invalid choices.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Search](binary-search.md) | [Patterns Index](index.md) | [DP - 1D](dp-1d.md) |

## When to Use

- Permutations.
- Combinations.
- Subsets.

## TypeScript Example

```ts
function subsets(nums: number[]): number[][] {
  const result: number[][] = [];

  function backtrack(start: number, path: number[]): void {
    result.push([...path]);

    for (let i = start; i < nums.length; i++) {
      path.push(nums[i]);
      backtrack(i + 1, path);
      path.pop();
    }
  }

  backtrack(0, []);
  return result;
}
```

## Complexity

- Time: depends on the solution space, often exponential.
- Space: recursion depth + current path.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=backtracking+leetcode
