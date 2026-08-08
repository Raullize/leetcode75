# Array / String

Arrays and strings are the foundation of most LeetCode 75 problems.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Patterns Index](index.md) | [Patterns Index](index.md) | [Two Pointers](two-pointers.md) |

## When to Use

- When the input is an indexable sequence.
- When you need to iterate, compare, transform, or reorganize elements.

## Common Patterns

- Traverse with `for` or `for...of`.
- Build a new answer with an accumulator.
- Convert a string to an array when it is useful.

## TypeScript Example

```ts
function reverseVowels(s: string): string {
  const vowels = new Set(['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U']);
  const chars = s.split('');
  let left = 0;
  let right = chars.length - 1;

  while (left < right) {
    while (left < right && !vowels.has(chars[left])) left++;
    while (left < right && !vowels.has(chars[right])) right--;

    [chars[left], chars[right]] = [chars[right], chars[left]];
    left++;
    right--;
  }

  return chars.join('');
}
```

## Key Idea

Use arrays and strings as building blocks for patterns like Two Pointers, Sliding Window, and Prefix Sum.

## Complexity

- Time: usually `O(n)`.
- Space: depends on the transformation, often `O(n)` if you create a copy.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=leetcode+array+string
