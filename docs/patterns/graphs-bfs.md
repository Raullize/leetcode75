# Graphs - BFS

BFS in graphs explores level by level from a source.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Graphs - DFS](graphs-dfs.md) | [Patterns Index](index.md) | [Heap / Priority Queue](heap-priority-queue.md) |

## When to Use

- Shortest number of steps in an unweighted graph.
- Minimum edge distance.

## TypeScript Example

```ts
function shortestPathUnweighted(n: number, edges: number[][], start: number, end: number): number {
  const graph: number[][] = Array.from({ length: n }, () => []);
  for (const [a, b] of edges) {
    graph[a].push(b);
    graph[b].push(a);
  }

  const queue: [number, number][] = [[start, 0]];
  const visited = new Set<number>([start]);

  while (queue.length > 0) {
    const [node, dist] = queue.shift()!;
    if (node === end) return dist;

    for (const next of graph[node]) {
      if (!visited.has(next)) {
        visited.add(next);
        queue.push([next, dist + 1]);
      }
    }
  }

  return -1;
}
```

## Complexity

- Time: `O(V + E)`.
- Space: `O(V)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=graph+bfs+leetcode
