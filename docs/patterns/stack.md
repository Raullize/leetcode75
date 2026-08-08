# Stack

Stack follows the LIFO rule: last in, first out.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Hash Map / Set](hash-map-set.md) | [Patterns Index](index.md) | [Queue](queue.md) |

## When to Use

- Valid parentheses.
- Undo operations.
- Expressions and reverse-order processing.

## TypeScript Example

```ts
function isValid(s: string): boolean {
  const stack: string[] = [];
  const pairs = new Map([
    [')', '('],
    [']', '['],
    ['}', '{'],
  ]);

  for (const char of s) {
    if (pairs.has(char)) {
      if (stack.pop() !== pairs.get(char)) return false;
    } else {
      stack.push(char);
    }
  }

  return stack.length === 0;
}
```

## Complexity

- Time: `O(n)`.
- Space: `O(n)` in the worst case.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=stack+leetcode
