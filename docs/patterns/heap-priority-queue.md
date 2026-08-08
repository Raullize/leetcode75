# Heap / Priority Queue

Heap allows fast access to the smallest or largest element.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Graphs - BFS](graphs-bfs.md) | [Patterns Index](index.md) | [Binary Search](binary-search.md) |

## When to Use

- Top K.
- Scheduling.
- Merging sorted lists.

## TypeScript Example

```ts
class MinHeap {
  private data: number[] = [];

  push(value: number): void {
    this.data.push(value);
    this.bubbleUp(this.data.length - 1);
  }

  pop(): number | undefined {
    if (this.data.length === 0) return undefined;
    const root = this.data[0];
    const last = this.data.pop()!;
    if (this.data.length > 0) {
      this.data[0] = last;
      this.bubbleDown(0);
    }
    return root;
  }

  private bubbleUp(index: number): void {
    while (index > 0) {
      const parent = Math.floor((index - 1) / 2);
      if (this.data[parent] <= this.data[index]) break;
      [this.data[parent], this.data[index]] = [this.data[index], this.data[parent]];
      index = parent;
    }
  }

  private bubbleDown(index: number): void {
    while (true) {
      let smallest = index;
      const left = index * 2 + 1;
      const right = index * 2 + 2;

      if (left < this.data.length && this.data[left] < this.data[smallest]) smallest = left;
      if (right < this.data.length && this.data[right] < this.data[smallest]) smallest = right;
      if (smallest === index) break;

      [this.data[index], this.data[smallest]] = [this.data[smallest], this.data[index]];
      index = smallest;
    }
  }
}
```

## Complexity

- Insert: `O(log n)`.
- Remove top: `O(log n)`.
- Peek top: `O(1)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=heap+priority+queue+leetcode
