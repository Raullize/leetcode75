# Array / String - Easy Exercise

Practice problem to validate the Array / String pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Exercises Index](index.md) | [Exercises Index](index.md) | [Two Pointers](two-pointers.md) |

## Pattern Reference

- [Array / String](../patterns/array-string.md)

## Problem

[Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/) — Difficulty: Easy

## Statement

You are given two strings `word1` and `word2`. Merge the strings by adding letters in alternating order, starting with `word1`. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.

## Examples

```
word1 = "abc", word2 = "pqr"   -> "apbqcr"
word1 = "ab",  word2 = "pqrs"  -> "apbqrs"
word1 = "abcd", word2 = "pq"   -> "apbqcd"
```

## Constraints

- `1 <= word1.length, word2.length <= 100`
- `word1` and `word2` consist of lowercase English letters.

## What This Validates

- Iterating over two indexable sequences in parallel.
- Handling the leftover tail when lengths differ.

## Hint

<details>
<summary>Hint</summary>

Loop while either string still has characters left. On each iteration, pick the next character from the current string if it exists, then move to the other string.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Handles different lengths correctly.
- [ ] Explained the approach out loud.
- [ ] Identified the time and space complexity.