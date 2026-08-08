# Binary Tree - BFS

BFS in a tree traverses level by level.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Tree - DFS](binary-tree-dfs.md) | [Patterns Index](index.md) | [Binary Search Tree](binary-search-tree.md) |

## When to Use

- Closest level.
- Tree width.
- Layered processing.

## TypeScript Example

```ts
function levelOrder(root: TreeNode | null): number[][] {
  if (!root) return [];

  const result: number[][] = [];
  const queue: TreeNode[] = [root];
  let head = 0;

  while (head < queue.length) {
    const size = queue.length - head;
    const level: number[] = [];

    for (let i = 0; i < size; i++) {
      const node = queue[head++];
      level.push(node.val);
      if (node.left) queue.push(node.left);
      if (node.right) queue.push(node.right);
    }

    result.push(level);
  }

  return result;
}
```

## Complexity

- Time: `O(n)`.
- Space: `O(w)` where `w` is the maximum width.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=binary+tree+bfs+leetcode
