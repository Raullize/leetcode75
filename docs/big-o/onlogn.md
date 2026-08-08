# O(n log n) - Linearithmic

Combines a linear traversal with a logarithmic split.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(n)](on.md) | [Big O Index](index.md) | [O(n^2)](on2.md) |

## Example

```ts
function sortAndMap(nums: number[]): number[] {
  return nums.sort((a, b) => a - b).map((x) => x * 2);
}
```

## When it Appears

- Efficient sorting.
- Heapify and batch heap operations.
- Well-optimized divide and conquer algorithms.

## Intuition

This grows above `O(n)`, but is still much better than `O(n^2)` for large inputs.
