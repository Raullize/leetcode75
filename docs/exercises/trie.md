# Trie - Easy Exercise

Practice problem to validate the Trie pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Bit Manipulation](bit-manipulation.md) | [Exercises Index](index.md) | [Intervals](intervals.md) |

## Pattern Reference

- [Trie](../patterns/trie.md)

## Problem

[Longest Word in Dictionary](https://leetcode.com/problems/longest-word-in-dictionary/) — Difficulty: Easy

## Statement

Given an array of strings `words` representing an English dictionary, return the longest word in `words` that can be built one character at a time by other words in `words`.

A word can be built one character at a time if every prefix of the word is present in `words`.

If there is more than one possible answer, return the longest word with the smallest lexicographical order. If there is no answer, return the empty string.

## Examples

```
words = ["w","wo","wor","worl","world"] -> "world"
words = ["a","banana","app","appl","ap","apply","apple"] -> "apple"
```

## Constraints

- `1 <= words.length <= 1000`
- `1 <= words[i].length <= 30`
- All `words[i]` consist of lowercase English letters.

## What This Validates

- Building a trie and traversing it by prefixes.
- Checking that every prefix of a candidate word exists.

## Hint

<details>
<summary>Hint</summary>

Insert all words into a trie, marking each node that ends a word. Then DFS from the root, only descending into child nodes that also end a word. Track the longest such path; on ties, pick the lexicographically smallest word.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Understands why every prefix must be present.
- [ ] Handles the lexicographical tie-break correctly.
- [ ] Explained the approach out loud.