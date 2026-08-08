# Linked List

Linked List is a chained structure where each node points to the next.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Queue](queue.md) | [Patterns Index](index.md) | [Binary Tree - DFS](binary-tree-dfs.md) |

## When to Use

- Local insertions and removals.
- Problems involving cycles, reversal, and merge.

## TypeScript Example

```ts
class ListNode {
  val: number;
  next: ListNode | null;

  constructor(val: number, next: ListNode | null = null) {
    this.val = val;
    this.next = next;
  }
}

function reverseList(head: ListNode | null): ListNode | null {
  let prev: ListNode | null = null;
  let curr = head;

  while (curr) {
    const next = curr.next;
    curr.next = prev;
    prev = curr;
    curr = next;
  }

  return prev;
}
```

## Complexity

- Time: `O(n)`.
- Space: `O(1)` for iterative reversal.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=linked+list+leetcode
