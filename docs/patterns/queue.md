# Queue

Queue follows the FIFO rule: first in, first out.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Stack](stack.md) | [Patterns Index](index.md) | [Linked List](linked-list.md) |

## When to Use

- BFS.
- Arrival-order processing.
- Queue simulation.

## TypeScript Example

```ts
class Queue<T> {
  private data: T[] = [];
  private head = 0;

  enqueue(value: T): void {
    this.data.push(value);
  }

  dequeue(): T | undefined {
    if (this.head >= this.data.length) return undefined;
    const value = this.data[this.head];
    this.head++;
    return value;
  }

  peek(): T | undefined {
    return this.head < this.data.length ? this.data[this.head] : undefined;
  }

  get length(): number {
    return this.data.length - this.head;
  }
}
```

## Complexity

- Enqueue: `O(1)`.
- Dequeue: `O(1)` with a head pointer.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=queue+leetcode
