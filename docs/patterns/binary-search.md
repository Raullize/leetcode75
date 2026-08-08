# Binary Search

Binary Search searches an ordered structure by halving the search space.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Heap / Priority Queue](heap-priority-queue.md) | [Patterns Index](index.md) | [Backtracking](backtracking.md) |

## When to Use

- Sorted array.
- Monotonic answer.
- Optimization problems with a true/false condition.

## TypeScript Example

```ts
function search(nums: number[], target: number): number {
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

## Mental Rule

Always ask: does the condition improve when I go left or right?

## Complexity

- Time: `O(log n)`.
- Space: `O(1)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=binary+search+leetcode
