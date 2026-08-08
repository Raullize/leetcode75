# O(2^n) - Exponencial

The number of possibilities doubles at each step.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(n^2)](on2.md) | [Big O Index](index.md) | [O(n!)](on-factorial.md) |

## Example

```ts
function fib(n: number): number {
  if (n <= 1) return n;
  return fib(n - 1) + fib(n - 2);
}
```

## When it Appears

- Naive recursion.
- Choosing or not choosing an element.
- Decision trees with a constant branching factor.

## Intuition

This cost grows very quickly. In real problems, you usually need memoization or another optimization.
