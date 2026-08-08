# O(log n) - Logarithmic

Each step reduces the problem by half or by a fixed fraction.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(1)](o1.md) | [Big O Index](index.md) | [O(n)](on.md) |

## Example

```ts
function binarySearch(nums: number[], target: number): number {
  let left = 0;
  let right = nums.length - 1;

  while (left <= right) {
    const mid = Math.floor((left + right) / 2);
    if (nums[mid] === target) return mid;
    if (nums[mid] < target) left = mid + 1;
    else right = mid - 1;
  }

  return -1;
}
```

## When it Appears

- Binary Search.
- Balanced tree.
- Heap insertion and removal operations.

## Intuition

If the input has 1,000,000 items and you remove half at each step, the number of steps grows slowly.
