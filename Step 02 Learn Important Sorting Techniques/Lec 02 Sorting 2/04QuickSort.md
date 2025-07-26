# Lecture 02: Quick Sort in JavaScript ⚡🔢

Quick Sort is a highly efficient sorting algorithm based on the divide-and-conquer principle. It works by selecting a "pivot" element, partitioning the array around the pivot, and then recursively sorting the subarrays.

## How Quick Sort Works? 🤔

1. **Choose a Pivot:**  
   Select an element from the array as the pivot (commonly the first or last element).
2. **Partition:**  
   Rearrange the array so that all elements less than or equal to the pivot are on its left, and all elements greater are on its right.
3. **Recursively Sort:**  
   Recursively apply the above steps to the subarrays on the left and right of the pivot.

## Step-by-Step Example 📝

Given: `[4, 6, 2, 5, 7, 9, 1, 3]`

- Select a pivot (e.g., 4).
- Partition the array around the pivot.
- Recursively sort the left and right subarrays.

## Code Implementation 💻

```javascript
let arr = [4, 6, 2, 5, 7, 9, 1, 3];
let n = arr.length;

function quickSort(arr, low, high){
    if(low < high){
        let partitionIndex = partitionFinder(arr, low, high);
        quickSort(arr, low, partitionIndex-1);
        quickSort(arr, partitionIndex+1, high);
    }
}

function partitionFinder(arr, low, high){
    let pivot = arr[low];
    let i = low;
    let j = high;
    while(i < j){
        while(arr[i] <= pivot && i <= high-1) i++;
        while(arr[j] > pivot && j >= low+1 ) j--;
        if(i < j) [arr[i], arr[j]] = [arr[j], arr[i]];
    }
    [arr[low], arr[j]] = [arr[j], arr[low]];
    return j;
}

console.log("Before sorting:", arr);
quickSort(arr, 0, n-1);
console.log("After sorting:", arr); // Output: [1, 2, 3, 4, 5, 6, 7, 9]
```

## Time Complexity ⏳

- **Best & Average Case:** O(n log n)
- **Worst Case:** O(n²) (when the smallest or largest element is always chosen as pivot)
- **Space Complexity:** O(log n) (due to recursion stack)

## Summary 🎉

- Quick Sort is fast and efficient for large datasets.
- Uses partitioning and recursion to sort arrays.
- The choice of pivot can significantly affect performance.