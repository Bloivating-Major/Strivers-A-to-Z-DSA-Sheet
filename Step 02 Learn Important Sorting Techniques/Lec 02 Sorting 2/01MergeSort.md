# Lecture 02: Merge Sort in JavaScript 🧩🔢

Merge Sort is a powerful and efficient sorting algorithm based on the divide-and-conquer principle. It divides the array into halves, sorts each half recursively, and then merges the sorted halves to produce the final sorted array.

## How Merge Sort Works? 🤔

1. **Divide:** Split the array into two halves.
2. **Conquer:** Recursively sort each half.
3. **Combine:** Merge the two sorted halves into a single sorted array.

## Step-by-Step Example 📝

Given: `[3, 1, 2, 4, 1, 5, 2, 6, 4]`

- Divide the array into smaller subarrays until each subarray has one element.
- Merge subarrays in sorted order until the whole array is sorted.

## Code Implementation 💻

```javascript
let arr = [3, 1, 2, 4, 1, 5, 2, 6, 4];

function merge(arr, low, mid, high){
    let temp = [];
    let left = low;
    let right = mid+1;
    
    while(left <= mid && right <= high){
        if(arr[left] < arr[right]){
            temp.push(arr[left]);
            left++;
        }else{
            temp.push(arr[right]);
            right++;
        }
    }
    
    while(left <= mid){
        temp.push(arr[left]);
        left++;
    }
    
    while(right <= high){
        temp.push(arr[right]);
        right++;
    }
    
    for(let i = low; i <= high; i++){
        arr[i] = temp[i-low];
    }
}

function mS(arr, low, high){
    if(low >= high) return;
    let mid = Math.floor((low + high) / 2);
    mS(arr, low, mid);
    mS(arr, mid+1, high);
    merge(arr, low, mid, high);
};

console.log("Before sorting:", arr);

mS(arr, 0, arr.length-1);

console.log("After sorting:", arr); // Output: [1, 1, 2, 2, 3, 4, 4, 5, 6]
```

## Time Complexity ⏳

- **Best, Average, Worst Case:** O(n log n)
- **Space Complexity:** O(n) (extra space for merging)

## Summary 🎉

- Merge Sort is efficient and stable, making it great for large datasets.
- It uses recursion and merging to sort arrays.
- The divide-and-conquer approach ensures a consistent O(n log n) time complexity.