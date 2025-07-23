# Lecture 05: Reverse an Array Using Recursion 🔄🧩

Reversing an array is a classic problem in programming! Using recursion to reverse an array helps you understand how recursive calls work with indices and swapping.

## What Does "Reverse an Array" Mean? 🤔

- Given an array, you want to rearrange its elements so the first becomes last, the second becomes second-last, and so on.
- Example:  
  `[1, 2, 3, 4, 5]` → `[5, 4, 3, 2, 1]`

## Recursive Approach 🔁

- Swap the first and last elements.
- Recursively reverse the subarray between them.
- Stop when the start index is greater than or equal to the end index (base case).

## Step-by-Step Algorithm 📝

1. Define a function that takes the array, a start index, and an end index.
2. If `start >= end`, stop (base case).
3. Swap `arr[start]` and `arr[end]`.
4. Recursively call the function with `start + 1` and `end - 1`.

## Example Code 💻

```javascript
function reverseArray(arr, start = 0, end = arr.length - 1) {
  // Base case: stop when start >= end
  if (start >= end) return;

  // Swap elements at start and end
  [arr[start], arr[end]] = [arr[end], arr[start]];

  // Recursive call for the next pair
  reverseArray(arr, start + 1, end - 1);
}

// Usage example
let numbers = [1, 2, 3, 4, 5];
reverseArray(numbers);
console.log(numbers); // Output: [5, 4, 3, 2, 1]
```

## How Does It Work? 🛠️

- The function swaps the outer elements and moves inward.
- Each recursive call works on a smaller subarray.
- When the indices meet or cross, recursion stops!

## Creative Twist: Reverse with Emojis 🎨

```javascript
let emojis = ["😀", "🐱", "🍕", "🚀", "🌟"];
reverseArray(emojis);
console.log(emojis); // Output: ["🌟", "🚀", "🍕", "🐱", "😀"]
```

## Summary 🎉

- Recursion is a fun and elegant way to reverse arrays.
- Always set a base case to avoid infinite recursion.
- Try reversing arrays of numbers, strings, or even emojis to see how it works!