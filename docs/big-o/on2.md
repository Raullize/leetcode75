# O(n^2) - Quadratic

It usually appears in two nested loops.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(n log n)](onlogn.md) | [Big O Index](index.md) | [O(2^n)](o2n.md) |

## Example

```ts
function pairSums(nums: number[]): number[] {
  const result: number[] = [];
  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      result.push(nums[i] + nums[j]);
    }
  }
  return result;
}
```

## When it Appears

- All-pairs comparisons.
- Some interval problems without preprocessing.
- Brute-force array solutions.

## Intuition

If doubling the input tends to multiply the time by four, you are close to `O(n^2)`.
