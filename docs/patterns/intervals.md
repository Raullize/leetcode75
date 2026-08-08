# Intervals

Intervals appear when you need to sort, merge, or detect overlap among segments.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Trie](trie.md) | [Patterns Index](index.md) | [Monotonic Stack](monotonic-stack.md) |

## When to Use

- Calendars.
- Time ranges.
- Merging overlapping segments.

## TypeScript Example

```ts
function merge(intervals: number[][]): number[][] {
  if (intervals.length === 0) return [];

  intervals.sort((a, b) => a[0] - b[0]);
  const result: number[][] = [intervals[0]];

  for (let i = 1; i < intervals.length; i++) {
    const last = result[result.length - 1];
    const current = intervals[i];

    if (current[0] <= last[1]) {
      last[1] = Math.max(last[1], current[1]);
    } else {
      result.push(current);
    }
  }

  return result;
}
```

## Key Rule

Sorting first usually simplifies interval logic a lot.

## Complexity

- Time: `O(n log n)` because of sorting.
- Space: `O(n)` for the output.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=intervals+leetcode
