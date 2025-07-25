# Lecture 01: Bubble Sort in JavaScript 🫧🔢

Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The process is repeated until the array is sorted.

## How Bubble Sort Works? 🤔

1. Start from the beginning of the array.
2. Compare each pair of adjacent elements.
3. If the first element is greater than the second, swap them.
4. Repeat this process for all elements, pushing the largest element to the end in each pass (like a bubble rising to the top).
5. Continue until no swaps are needed, meaning the array is sorted.

## Step-by-Step Example 📝

Given: `[10, 5, 1, 12, 3, 44, 2, 4, 8]`

- Compare and swap adjacent elements.
- After each pass, the largest unsorted element moves to its correct position at the end.

## Code Implementation 💻

```javascript
let arr = [10, 5, 1, 12, 3, 44, 2, 4, 8];
let n = arr.length;

for(let i = 0; i < n - 1; i++){
    for(let j = 0; j < n - 1 - i; j++){
        if(arr[j] > arr[j+1]){
            [arr[j], arr[j+1]] = [arr[j+1], arr[j]];
        }
    }
}

console.log(arr); // Output: [1, 2, 3, 4, 5, 8, 10, 12, 44]
```

## Time Complexity ⏳

- **Best Case:** O(n) (when the array is already sorted)
- **Average & Worst Case:** O(n²)
- **Space Complexity:** O(1) (in-place sorting)

## Summary 🎉

- Bubble Sort is easy to understand and implement.
- Not efficient for large arrays, but great for learning sorting basics!
- Each pass "bubbles" the largest unsorted element to its correct position.