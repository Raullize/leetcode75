# Graphs - DFS

DFS in graphs explores deeply before backtracking.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Search Tree](binary-search-tree.md) | [Patterns Index](index.md) | [Graphs - BFS](graphs-bfs.md) |

## When to Use

- Connected components.
- Cycles.
- Path search.

## TypeScript Example

```ts
function countComponents(n: number, edges: number[][]): number {
  const graph: number[][] = Array.from({ length: n }, () => []);
  for (const [a, b] of edges) {
    graph[a].push(b);
    graph[b].push(a);
  }

  const visited = new Set<number>();

  function dfs(node: number): void {
    visited.add(node);
    for (const next of graph[node]) {
      if (!visited.has(next)) dfs(next);
    }
  }

  let components = 0;
  for (let i = 0; i < n; i++) {
    if (!visited.has(i)) {
      components++;
      dfs(i);
    }
  }

  return components;
}
```

## Complexity

- Time: `O(V + E)`.
- Space: `O(V)`.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=graph+dfs+leetcode
