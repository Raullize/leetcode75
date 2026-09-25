# Stack - Easy Exercise

Practice problem to validate the Stack pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Hash Map / Set](hash-map-set.md) | [Exercises Index](index.md) | [Queue](queue.md) |

## Pattern Reference

- [Stack](../patterns/stack.md)

## Problem

[Remove Outermost Parentheses](https://leetcode.com/problems/remove-outermost-parentheses/) — Difficulty: Easy

## Statement

A valid parentheses string is either empty `""`, `"(" + A + ")"`, or `A + B`, where `A` and `B` are valid parentheses strings, and `+` represents string concatenation.

A valid parentheses string is **primitive** if it is nonempty and there is no way to split it into `A + B`, with `A` and `B` nonempty valid parentheses strings.

Given a valid parentheses string `s`, return the result of removing the outermost parentheses of every primitive string in the primitive decomposition of `s`.

## Examples

```
s = "(()())(())"            -> "()()()"
s = "(()())(())(()(()))"    -> "()()()()(())"
s = "()()"                  -> ""
```

## Constraints

- `1 <= s.length <= 10^5`
- `s[i]` is either `'('` or `')'`.
- `s` is a valid parentheses string.

## What This Validates

- Using a stack (or a depth counter) to track nesting depth.
- Recognizing when the outermost pair can be skipped.

## Hint

<details>
<summary>Hint</summary>

Track the current depth as you scan. When you see an opening parenthesis that makes the depth go from `0` to `1`, it is an outer parenthesis — skip it. Every other parenthesis is part of the inner content and should be kept.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Achieves `O(n)` time.
- [ ] Correctly keeps the inner content of every primitive string.
- [ ] Explained the approach out loud.