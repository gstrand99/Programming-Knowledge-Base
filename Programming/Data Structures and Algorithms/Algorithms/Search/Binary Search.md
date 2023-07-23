- the array must be sorted
## [[Big O]]
- O(N) or linear time complexity when going by 10 % each time
- time complexity wasn't improved when cutting stuff in half because it is still constant, but it would be practically faster
- O(logN) when halving each time

## Code
``` typescript
 export default function bs_list(haystack: number[], needle: number): boolean {

  let low = 0;
  let high = haystack.length;

  do {
    const middle = Math.floor(low + (high - low) / 2);
    const value = haystack[middle]

    if (value == needle) {
      return true;
    } else if (value > needle) {
      high = middle
    } else {
      low = middle + 1
    }

  } while (low < high);

  return false
}
```