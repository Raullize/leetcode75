# Cheat Sheet

Quick reference to recognize LeetCode 75 patterns and the most common Big O cases.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [README](../README.md) | [README](../README.md) | [Big O Index](big-o/index.md) |

## Big O in One Line

- `O(1)`: direct access, local state.
- `O(log n)`: divides the problem in half.
- `O(n)`: scans the input once.
- `O(n log n)`: sorting or efficient divide and conquer.
- `O(n^2)`: pair comparisons or two loops.
- `O(2^n)`: binary choices per step.
- `O(n!)`: full permutations.
- `O(sqrt n)`: divisor search / primality.

## Common Patterns

- `Array / String`: linear sequence, transformation, iteration.
- `Two Pointers`: compare ends or use pointers at different speeds.
- `Sliding Window`: contiguous subarray / substring with a fixed or variable window.
- `Prefix Sum`: many interval sum queries.
- `Hash Map / Set`: fast lookup, counting, deduplication.
- `Stack`: LIFO, parentheses, reversal, cancellation.
- `Queue`: FIFO, BFS, ordered processing.
- `Linked List`: local insertions/removals, reversal, cycles.
- `Binary Tree - DFS`: depth, height, path.
- `Binary Tree - BFS`: level by level, width.
- `Binary Search Tree`: search in an ordered tree.
- `Graphs - DFS`: components, cycles, deep exploration.
- `Graphs - BFS`: shortest path in an unweighted graph.
- `Heap / Priority Queue`: top k, scheduling, next min/max.
- `Binary Search`: search in an ordered structure or monotonic answer space.
- `Backtracking`: explore choices and undo them.
- `DP - 1D`: state in one dimension.
- `DP - Multidimensional`: state in a grid or with more than one variable.
- `Bit Manipulation`: XOR, flags, parity.
- `Trie`: prefixes, autocomplete, dictionary.
- `Intervals`: merge, overlap, calendar.
- `Monotonic Stack`: next greater/smaller, histogram.

## How to Think Quickly

1. Is the input a sequence? think Array/String, Two Pointers, Sliding Window, or Prefix Sum.
2. Do you need fast existence checks? think Hash Map / Set.
3. Does the problem involve processing order? think Stack or Queue.
4. Is the structure a tree or graph? choose DFS or BFS.
5. Is there an ordering property? think Binary Search or BST.
6. Do you need to explore combinations? think Backtracking.
7. Does the state depend on previous results? think DP.
