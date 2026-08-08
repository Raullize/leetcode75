# Two Pointers

Two Pointers uses two indices to explore the structure efficiently.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Array / String](array-string.md) | [Patterns Index](index.md) | [Sliding Window](sliding-window.md) |

## When to Use

- Sorted arrays or strings.
- Comparison between ends.
- Reducing an `O(n^2)` search to `O(n)`.

## TypeScript Example

```ts
function isPalindrome(s: string): boolean {
  let left = 0;
  let right = s.length - 1;

  while (left < right) {
    while (left < right && !/[a-z0-9]/i.test(s[left])) left++;
    while (left < right && !/[a-z0-9]/i.test(s[right])) right--;

    if (s[left].toLowerCase() !== s[right].toLowerCase()) return false;
    left++;
    right--;
  }

  return true;
}
```

## Variations

- Pointers at both ends.
- Pointers moving at different speeds.
- Read and write pointers.

## Complexity

- Time: `O(n)`.
- Space: `O(1)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=two+pointers+leetcode
