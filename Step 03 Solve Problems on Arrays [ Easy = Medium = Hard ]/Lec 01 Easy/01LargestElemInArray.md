# Lecture 01: Find the Largest Element in an Array 🚀🔢

Finding the largest element in an array is a fundamental problem in programming. There are multiple ways to solve this, including brute force and optimized approaches.

## Brute Force Approach 🐢

- Sort the array in ascending order.
- The largest element will be at the last index.

```javascript
let arr = [2, 3, 5, 6, 9, 4];

// Brute Force
arr.sort((a, b) => a - b);
let largest = arr[arr.length - 1];

console.log(largest); // Output: 9
```

## Optimized Approach ⚡

- Traverse the array once and keep track of the maximum value.

```javascript
let arr = [2, 3, 5, 6, 9, 4];
let largest = arr[0];

for (let i = 1; i < arr.length; i++) {
  if (arr[i] > largest) {
    largest = arr[i];
  }
}

console.log(largest); // Output: 9
```

## Summary 🎉

- Brute force uses sorting, which is less efficient (O(n log n)).
- Optimized approach finds the largest in a single pass (O(n)).
- Always prefer the optimized approach for better performance.