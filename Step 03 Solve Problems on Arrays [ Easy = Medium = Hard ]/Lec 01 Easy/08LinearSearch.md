# Lecture 01: Linear Search in an Array 🔍🔢

Linear Search is the simplest searching algorithm. It checks each element of the array sequentially until the target value is found or the end of the array is reached.

## Problem Statement 🤔

- Given an array and a target value, find the index of the target in the array.
- If the target is not found, return -1.

## How Linear Search Works? 🚀

1. Start from the first element of the array.
2. Compare each element with the target value.
3. If a match is found, return the index.
4. If the end of the array is reached and no match is found, return -1.

## Code Implementation 💻

```javascript
let target = 5;
let arr = [1, 2, 3, 4, 5];

for(let i = 0; i < arr.length; i++){
    if(arr[i] === target){
        console.log("Found target at index:", i);
        // You can return i here if using a function
    }
}

return -1; // If not found
```

## Summary 🎉

- Linear Search is easy to implement and works on unsorted arrays.
- Time Complexity: O(n)
- Space Complexity: O(1)
- Useful for small datasets or when simplicity is preferred over efficiency.

- Not suitable for large datasets due to its linear time complexity.