# Lecture 01: Insertion Sort in JavaScript 📝🔢

Insertion Sort is a simple and intuitive sorting algorithm. It builds the sorted array one element at a time by inserting each new element into its correct position among the previously sorted elements.

## How Insertion Sort Works? 🤔

1. Start from the second element (index 1) and treat the first element as a sorted subarray.
2. Pick the current element (key) and compare it with elements in the sorted subarray (to its left).
3. Shift all elements greater than the key one position to the right.
4. Insert the key at its correct position.
5. Repeat for all elements until the array is sorted.

## Step-by-Step Example 📝

Given: `[10, 5, 12, 1, 3]`

- Start with the second element (5), compare with 10, and insert in the correct position.
- Continue for each element, shifting and inserting as needed.

## Code Implementation 💻

```javascript
let arr = [10, 5, 12, 1, 3];
let n = arr.length;

console.log("Before sorting:", arr);

// Insertion Sort
for(let i = 1; i < n; i++){
    let key = arr[i];
    let j = i - 1;
    while(j >= 0 && arr[j] > key){
        arr[j+1] = arr[j];
        j--;
    }
    // when j becomes -1 or arr[j] is less than key, insert key
    arr[j+1] = key;
}

console.log("After sorting:", arr); // Output: [1, 3, 5, 10, 12]
```

## Time Complexity ⏳

- **Best Case:** O(n) (already sorted array)
- **Average & Worst Case:** O(n²)
- **Space Complexity:** O(1) (in-place sorting)

## Summary 🎉

- Insertion Sort is efficient for small or nearly sorted arrays.
- It sorts the array by inserting each element into its correct position.
- Easy to implement and understand, making it a great choice for learning sorting algorithms!