## How does it work?
- [[Trees]]
![[Tree Traversal.png]]
 # Depth First Orders
- Pre 
```typescript
function walk(curr: BinaryNode<number> | null, path: number[]): number[] {
  if (!curr) {
    return path;
  }

  path.push(curr.value);

  walk(curr.left, path);
  walk(curr.right, path);

  return path;
}

export default function pre_order_search(head: BinaryNode<number>): number[] {
  return walk(head, []);
}
```
- In
```typescript
function walk(curr: BinaryNode<number> | null, path: number[]): number[] {
  if (!curr) {
    return path;
  }
  
  walk(curr.left, path);
  path.push(curr.value);
  walk(curr.right, path);

  return path;
}

export default function pre_order_search(head: BinaryNode<number>): number[] {
  return walk(head, []);
}
```
- Post
```typescript
function walk(curr: BinaryNode<number> | null, path: number[]): number[] {
  if (!curr) {
    return path;
  }
  
  walk(curr.left, path);
  walk(curr.right, path);
  
  path.push(curr.value);

  return path;
}

export default function pre_order_search(head: BinaryNode<number>): number[] {
  return walk(head, []);
}
```