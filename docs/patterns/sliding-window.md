# Sliding Window

Sliding Window keeps an active window over a sequence to avoid recomputing everything from scratch.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Two Pointers](two-pointers.md) | [Patterns Index](index.md) | [Prefix Sum](prefix-sum.md) |

## When to Use

- Contiguous subarray or substring.
- Questions about maximum, minimum, sum, or frequency within a range.

## TypeScript Example

```ts
function maxAverage(nums: number[], k: number): number {
  let windowSum = 0;

  for (let i = 0; i < k; i++) windowSum += nums[i];

  let best = windowSum;

  for (let right = k; right < nums.length; right++) {
    windowSum += nums[right];
    windowSum -= nums[right - k];
    best = Math.max(best, windowSum);
  }

  return best / k;
}
```

## Types

- Fixed window: constant size.
- Variable window: expands and contracts based on a condition.

## Complexity

- Time: `O(n)`.
- Space: `O(1)` or `O(k)` if counters are needed.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=sliding+window+leetcode
