![[Two Crystal Ball.png]]

## [[Big O]]
- both binary search and linear search will be O(N)
	- linear is always O(N)
	- binary is 0(N) because if you break a crystal ball, you will have to then linear search
- square root of N

## Code
``` typescript
export default function two_crystal_balls(breaks: boolean[]): number {

  const jumpAmount = Math.floor(Math.sqrt(breaks.length));

  let i = jumpAmount;
  for (; i < breaks.length; i += jumpAmount) {
    if (breaks[i]) {
      break;
    }
  }

  i -= jumpAmount

  for (let j = 0; j < jumpAmount && i <breaks.length; ++j, ++i) {
    if (breaks[i]) {
      return i
    }
  }

  return -1;

}
```
