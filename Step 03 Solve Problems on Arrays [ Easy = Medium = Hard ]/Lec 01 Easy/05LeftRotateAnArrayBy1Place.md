# Lecture 01: Left Rotate an Array by 1 Place 🔄⬅️

Left rotation of an array by 1 place means shifting each element one position to the left, and moving the first element to the end of the array.

## Problem Statement 🤔

- Given an array, rotate it to the left by one position.
- Example: `[1, 2, 3, 4, 5]` → `[2, 3, 4, 5, 1]`

## Approach 🚀

1. Store the first element in a temporary variable.
2. Shift all other elements one position to the left.
3. Place the first element at the end of the array.

## Code Implementation 💻

```javascript
let arr = [1,2,3,4,5];

console.log("Before rotation:", arr);

let temp = arr[0];

for(let i = 1; i < arr.length; i++){
    arr[i-1] = arr[i]; 
}

arr[arr.length-1] = temp;

console.log("After rotation:", arr); // Output: [2, 3, 4, 5, 1]
```

## Summary 🎉

- Left rotation by 1 is a simple array manipulation.
- Useful in problems involving circular arrays or queues.