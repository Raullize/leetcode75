# Monotonic Stack

Monotonic Stack keeps the stack strictly increasing or decreasing.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Intervals](intervals.md) | [Patterns Index](index.md) | [README](../../README.md) |

## When to Use

- Next greater element.
- Next smaller element.
- Histogram problems.

## TypeScript Example

```ts
function nextGreaterElements(nums: number[]): number[] {
  const result = Array(nums.length).fill(-1);
  const stack: number[] = [];

  for (let i = 0; i < nums.length; i++) {
    while (stack.length > 0 && nums[i] > nums[stack[stack.length - 1]]) {
      const index = stack.pop()!;
      result[index] = nums[i];
    }
    stack.push(i);
  }

  return result;
}
```

## Key Idea

The stack stores candidates that are not resolved yet.

## Complexity

- Time: amortized `O(n)`.
- Space: `O(n)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=monotonic+stack+leetcode
