# Hash Map / Set

Hash Map and Set are essential for fast lookup, counting, and deduplication.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Prefix Sum](prefix-sum.md) | [Patterns Index](index.md) | [Stack](stack.md) |

## When to Use

- Knowing whether a value has appeared before.
- Counting frequencies.
- Mapping a key to information.

## TypeScript Example

```ts
function twoSum(nums: number[], target: number): number[] {
  const seen = new Map<number, number>();

  for (let i = 0; i < nums.length; i++) {
    const need = target - nums[i];
    if (seen.has(need)) {
      return [seen.get(need)!, i];
    }
    seen.set(nums[i], i);
  }

  return [];
}
```

## Practical Difference

- `Map`: key -> value.
- `Set`: element presence only.

## Complexity

- Average time: `O(1)` per operation.
- Total time: usually `O(n)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=hash+map+set+leetcode
