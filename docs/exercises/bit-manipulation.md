# Bit Manipulation - Easy Exercise

Practice problem to validate the Bit Manipulation pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [DP - Multidimensional](dp-multidimensional.md) | [Exercises Index](index.md) | [Trie](trie.md) |

## Pattern Reference

- [Bit Manipulation](../patterns/bit-manipulation.md)

## Problem

[Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/) — Difficulty: Easy

## Statement

Write a function that takes the binary representation of a positive integer and returns the number of **set bits** it has (also known as the Hamming weight).

## Examples

```
n = 11 (binary: 1011) -> 3
n = 128 (binary: 10000000) -> 1
n = 2147483645 (binary: 1111111111111111111111111111101) -> 30
```

## Constraints

- The input must be a binary string of length up to `32`.

## What This Validates

- Reading and clearing individual bits.
- The `n & (n - 1)` trick that removes the lowest set bit.

## Hint

<details>
<summary>Hint</summary>

You can check each bit with `n & 1` and shift with `n >>>= 1`. Faster: each `n & (n - 1)` removes exactly one set bit, so count how many times you can do it before `n` becomes `0`.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Handles the unsigned 32-bit input correctly.
- [ ] Identified the time and space complexity.
- [ ] Explained the approach out loud.