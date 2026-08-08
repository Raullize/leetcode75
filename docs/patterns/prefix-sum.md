# Prefix Sum

Prefix Sum stores cumulative sums to answer range queries quickly.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Sliding Window](sliding-window.md) | [Patterns Index](index.md) | [Hash Map / Set](hash-map-set.md) |

## When to Use

- Multiple sum queries over subarrays.
- Differences between positions.

## TypeScript Example

```ts
class NumArray {
  private prefix: number[];

  constructor(nums: number[]) {
    this.prefix = [0];
    for (const num of nums) {
      this.prefix.push(this.prefix[this.prefix.length - 1] + num);
    }
  }

  sumRange(left: number, right: number): number {
    return this.prefix[right + 1] - this.prefix[left];
  }
}
```

## Key Idea

If `prefix[i]` is the sum up to `i - 1`, then the sum of `left..right` is `prefix[right + 1] - prefix[left]`.

## Complexity

- Build: `O(n)`.
- Query: `O(1)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=prefix+sum+leetcode
