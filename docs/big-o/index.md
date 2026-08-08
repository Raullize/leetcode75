# Big O Notation

Big O describes how time or memory cost grows as the input size `n` increases.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Cheat Sheet](../cheat-sheet.md) | [Big O Index](index.md) | [O(1)](o1.md) |

## Core Idea

 - Ignore constants: `O(2n)` becomes `O(n)`.
 - Ignore smaller terms: `O(n^2 + n)` becomes `O(n^2)`.
 - Focus on the worst case unless stated otherwise.

## Analysis Cases

 - Best case: the most favorable scenario.
 - Average case: expected behavior in practice.
 - Worst case: the upper bound we usually use in LeetCode.

## Practical Rules

 - A single loop over the input is usually `O(n)`.
 - Halving the problem repeatedly is usually `O(log n)`.
 - Two nested loops suggest `O(n^2)`.
 - Recursion with two branches per level tends to be `O(2^n)`.
 - Full permutations tend to be `O(n!)`.

## Quick Examples

 - `O(1)`: access `nums[0]`.
 - `O(log n)`: binary search.
 - `O(n)`: sum all elements.
 - `O(n log n)`: sort and then iterate.
 - `O(n^2)`: compare all pairs.
 - `O(2^n)`: naive recursive fib.
 - `O(n!)`: generate permutations.
 - `O(sqrt n)`: primality test up to the square root.

## Case Index

- [O(1)](o1.md)
- [O(log n)](ologn.md)
- [O(n)](on.md)
- [O(n log n)](onlogn.md)
- [O(n^2)](on2.md)
- [O(2^n)](o2n.md)
- [O(n!)](on-factorial.md)
- [O(sqrt n)](osqrt-n.md)

## How to Study

Read each case separately to understand the growth pattern, a practical example, and where it appears in LeetCode problems.
