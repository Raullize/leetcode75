# O(n) - Linear

You traverse all elements once.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(log n)](ologn.md) | [Big O Index](index.md) | [O(n log n)](onlogn.md) |

## Example

```ts
function sum(nums: number[]): number {
  let total = 0;
  for (const num of nums) total += num;
  return total;
}
```

## When it Appears

- A single loop over an array, string, list, or tree.
- DFS and BFS visiting all nodes.

## Intuition

If doubling the input size tends to double the time, you are probably in `O(n)`.
