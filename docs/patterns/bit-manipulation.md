# Bit Manipulation

Bit manipulation uses binary operations to solve problems compactly and quickly.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [DP - Multidimensional](dp-multidimensional.md) | [Patterns Index](index.md) | [Trie](trie.md) |

## When to Use

- Parity.
- Flags.
- Small sets encoded in bits.

## TypeScript Example

```ts
function singleNumber(nums: number[]): number {
  let result = 0;
  for (const num of nums) result ^= num;
  return result;
}
```

## Useful Operations

- `&`: AND.
- `|`: OR.
- `^`: XOR.
- `<<`: left shift.
- `>>`: right shift.

## Complexity

- Time: `O(n)`.
- Space: `O(1)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=bit+manipulation+leetcode
