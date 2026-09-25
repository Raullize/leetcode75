# Heap / Priority Queue - Easy Exercise

Practice problem to validate the Heap / Priority Queue pattern.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Graphs - BFS](graphs-bfs.md) | [Exercises Index](index.md) | [Binary Search](binary-search.md) |

## Pattern Reference

- [Heap / Priority Queue](../patterns/heap-priority-queue.md)

## Problem

[Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/) — Difficulty: Easy

## Statement

Design a class to find the `kth` largest element in a stream. Note that it is the `kth` largest element in the sorted order, not the `kth` distinct element.

Implement `KthLargest`:

- `KthLargest(k, nums)` — initializes the object with the integer `k` and the stream of integers `nums`.
- `add(val)` — appends the integer `val` to the stream and returns the element representing the `kth` largest element in the stream.

## Examples

```
KthLargest kthLargest = new KthLargest(3, [4, 5, 8, 2]);
kthLargest.add(3);  // returns 4
kthLargest.add(5);  // returns 5
kthLargest.add(10); // returns 5
kthLargest.add(9);  // returns 8
kthLargest.add(4);  // returns 8
```

## Constraints

- `1 <= k <= 10^4`
- `0 <= nums.length <= 10^4`
- `-10^4 <= nums[i] <= 10^4`
- `-10^4 <= val <= 10^4`
- At most `10^4` calls will be made to `add`.
- It is guaranteed that there will be at least `k` elements in the array when you search for the `kth` element.

## What This Validates

- Keeping a min-heap of size `k` to track the `kth` largest efficiently.
- Why a heap beats sorting the whole stream on every `add`.

## Hint

<details>
<summary>Hint</summary>

Keep only the `k` largest elements in a min-heap. The top of the heap is always the `kth` largest. When adding, push the value, and if the heap exceeds `k` elements, pop the smallest one.

</details>

## Validation Checklist

- [ ] Solved without looking at the pattern example or a solution.
- [ ] Each `add` is `O(log k)`.
- [ ] Handles the initialization step correctly.
- [ ] Explained the approach out loud.