# O(n!) - Fatorial

It usually appears in full permutations.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [O(2^n)](o2n.md) | [Big O Index](index.md) | [O(sqrt n)](osqrt-n.md) |

## Example

```ts
function permute(nums: number[]): number[][] {
  const result: number[][] = [];

  function backtrack(path: number[], used: boolean[]): void {
    if (path.length === nums.length) {
      result.push([...path]);
      return;
    }

    for (let i = 0; i < nums.length; i++) {
      if (used[i]) continue;
      used[i] = true;
      path.push(nums[i]);
      backtrack(path, used);
      path.pop();
      used[i] = false;
    }
  }

  backtrack([], Array(nums.length).fill(false));
  return result;
}
```

## When it Appears

- Permutations.
- Brute-force TSP.
- Full exploration of element order.

## Intuition

This is explosive growth. Even for small `n`, the cost rises very quickly.
