# Binary Search Tree

BST maintains the property: left < node < right.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Binary Tree - BFS](binary-tree-bfs.md) | [Patterns Index](index.md) | [Graphs - DFS](graphs-dfs.md) |

## When to Use

- Efficient search in an ordered tree.
- Insertion and removal with ordered structure.

## TypeScript Example

```ts
function searchBST(root: TreeNode | null, val: number): TreeNode | null {
  if (!root || root.val === val) return root;
  if (val < root.val) return searchBST(root.left, val);
  return searchBST(root.right, val);
}
```

## Key Idea

BST reduces the search space like binary search, but on a tree.

## Complexity

- Best case: `O(log n)` in a balanced tree.
- Worst case: `O(n)` if it becomes skewed.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=binary+search+tree+leetcode
