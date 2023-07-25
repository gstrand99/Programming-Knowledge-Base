![[Linear Search.png]]

## [[Big O]]
- O(N) or a linear growth

## Code
``` typescript
export default function linear_search(haystack: number[], needle: number): boolean {

  for (let i = 0; i < haystack.length; ++i) {
    if (haystack[i] === needle) {
      return true;
    }
  }  
  return false
}
```