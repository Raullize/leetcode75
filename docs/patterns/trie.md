# Trie

Trie is a prefix tree for fast word and prefix searches.

## Navigation

| Previous | Home | Next |
| --- | --- | --- |
| [Bit Manipulation](bit-manipulation.md) | [Patterns Index](index.md) | [Intervals](intervals.md) |

## When to Use

- Word dictionaries.
- Autocomplete.
- Prefix search.

## TypeScript Example

```ts
class TrieNode {
  children: Map<string, TrieNode> = new Map();
  isWord = false;
}

class Trie {
  private root = new TrieNode();

  insert(word: string): void {
    let node = this.root;
    for (const char of word) {
      if (!node.children.has(char)) {
        node.children.set(char, new TrieNode());
      }
      node = node.children.get(char)!;
    }
    node.isWord = true;
  }

  search(word: string): boolean {
    const node = this.findNode(word);
    return node !== null && node.isWord;
  }

  startsWith(prefix: string): boolean {
    return this.findNode(prefix) !== null;
  }

  private findNode(prefix: string): TrieNode | null {
    let node = this.root;
    for (const char of prefix) {
      const next = node.children.get(char);
      if (!next) return null;
      node = next;
    }
    return node;
  }
}
```

## Complexity

- Insert: `O(L)`.
- Search: `O(L)`.
- `L` is the word length.

## YouTube Video

- Busca recomendada: https://www.youtube.com/results?search_query=trie+leetcode
