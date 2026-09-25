# Queue - Easy Exercise

Practice problem to validate the Queue pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Stack](stack.md) | [Exercises Index](index.md) | [Linked List](linked-list.md) |

## Pattern Reference

- [Queue](../patterns/queue.md)

## Problem

[Implement Queue using Stacks](https://leetcode.com/problems/implement-queue-using-stacks/) — Difficulty: Easy

## Statement

Implement a first in first out (FIFO) queue using only two stacks. The implemented queue should support all the functions of a normal queue:

- `push(x)` — push element `x` to the back of the queue.
- `pop()` — remove and return the element from the front of the queue.
- `peek()` — return the element at the front of the queue.
- `empty()` — return whether the queue is empty.

**Notes:** you must use only standard stack operations (push to top, peek/pop from top, size, and is empty).

## Examples

```
queue.push(1);
queue.push(2);
queue.peek(); // returns 1
queue.pop();  // returns 1
queue.empty(); // returns false
```

## Constraints

- `1 <= x <= 9`
- At most `100` calls will be made to push, pop, peek, and empty.
- All the calls to pop and peek are valid.

## What This Validates

- Understanding the difference between LIFO (Stack) and FIFO (Queue).
- Using two stacks to reverse an order.

## Hint

<details>
<summary>Hint</summary>

Use one stack for pushes and another stack that reverses the order. When you need to pop or peek, move everything from the input stack into the output stack — this flips the order so the front of the queue is on top. Only refill the output stack when it becomes empty.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] `pop()` and `peek()` are amortized `O(1)`.
- [ ] `empty()` works correctly.
- [ ] Explained the approach out loud.