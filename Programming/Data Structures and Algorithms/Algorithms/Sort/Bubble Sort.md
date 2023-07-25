![[Bubble Sort.png]]
## Explanation
- start at the beginning and ask if each number is larger than the number next to it
- first run always brings the largest number to the end and you can not check the final number

## [[Big O]]
![[bubble big o.png]]
- The whole if statement in this algo is constant so it gets dropped

## Code
``` typescript
export default function bubble_sort(arr: number[]): void {

  for (let i = 0; i < arr.length; ++i) {
    for (let j = 0; j < arr.length - i - i; ++j) {

      if (arr[j] > arr[j + 1]) {
        const tmp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = tmp;
      }
    }
  }
}
```