# Binary Tree - DFS

DFS in a tree explores one path to the end before backtracking.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Linked List](linked-list.md) | [Patterns Index](index.md) | [Binary Tree - BFS](binary-tree-bfs.md) |

## When to Use

- Tree height.
- Path sums.
- Depth-first search.

## TypeScript Example

```ts
class TreeNode {
  val: number;
  left: TreeNode | null;
  right: TreeNode | null;

  constructor(val: number, left: TreeNode | null = null, right: TreeNode | null = null) {
    this.val = val;
    this.left = left;
    this.right = right;
  }
}

function maxDepth(root: TreeNode | null): number {
  if (!root) return 0;
  return 1 + Math.max(maxDepth(root.left), maxDepth(root.right));
}
```

## Variations

- Preorder.
- Inorder.
- Postorder.

## Complexity

- Time: `O(n)`.
- Space: `O(h)` because of the recursion stack.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=binary+tree+dfs+leetcode
