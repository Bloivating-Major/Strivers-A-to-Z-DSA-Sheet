# Lecture 01: Selection Sort in JavaScript 🏆🔢

Selection Sort is a simple and intuitive sorting algorithm. It works by repeatedly finding the minimum element from the unsorted part of the array and putting it at the beginning.

## How Selection Sort Works? 🤔

1. Start from the first element and assume it's the minimum.
2. Compare this element with all other elements to find the actual minimum.
3. Swap the found minimum with the first element.
4. Move to the next position and repeat the process for the remaining unsorted part.
5. Continue until the array is sorted.

## Step-by-Step Example 📝

Given: `[10, 5, 1, 12, 3, 44, 2, 4, 8]`

- Find the smallest element and swap it with the first.
- Repeat for the rest of the array.

## Code Implementation 💻

```javascript
let arr = [10, 5, 1, 12, 3, 44, 2, 4, 8];
let n = arr.length;

for(let i = 0; i < n-1; i++){
    let minIndex = i;
    for(let j = i+1; j < n; j++){
        if(arr[minIndex] > arr[j]) minIndex = j;
    }
    if(minIndex !== i) [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]];
}

console.log(arr); // Output: [1, 2, 3, 4, 5, 8, 10, 12, 44]
```

## Time Complexity ⏳

- **Best, Average, Worst Case:** O(n²)
- **Space Complexity:** O(1) (in-place sorting)

## Summary 🎉

- Selection Sort is easy to understand and implement.
- Not the fastest for large arrays, but great for learning sorting basics!
- Always works in-place and does not require additional storage.