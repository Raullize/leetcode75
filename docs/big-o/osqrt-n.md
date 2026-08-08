# O(sqrt n) - Raiz Quadrada

It appears when the search can stop at the square root.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(n!)](on-factorial.md) | [Big O Index](index.md) | [Patterns Index](../patterns/index.md) |

## Example

```ts
function isPrime(n: number): boolean {
  if (n < 2) return false;
  for (let i = 2; i * i <= n; i++) {
    if (n % i === 0) return false;
  }
  return true;
}
```

## When it Appears

- Primality testing.
- Divisor search.
- Algorithms with quadratic-factor reduction.

## Intuition

You do not need to test all numbers up to `n`, only up to `sqrt(n)`.
