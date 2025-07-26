# Lecture 02: Recursive Bubble Sort in JavaScript 🔄🫧

Bubble Sort can also be implemented using recursion! Instead of using loops to process the array, we use recursive calls to sort the array step by step.

## Approach 🚀

1. **Recursive Range:**  
   Call the recursive function with the array and the current range (`n`).
2. **Swap Adjacent Elements:**  
   For the current range, swap adjacent elements if `arr[j] > arr[j+1]`.
3. **Recursive Call:**  
   After one pass, call the function again with the range reduced by 1 (`n-1`).
4. **Base Case:**  
   If the range is reduced to 1 (`n == 1`), stop recursion.

## Example Code 💻

```javascript
function recursiveBubbleSort(arr, n) {
  // Base case: if array size is 1, it's sorted
  if (n == 1) return;

  // One pass of bubble sort for current range
  for (let i = 0; i < n - 1; i++) {
    if (arr[i] > arr[i + 1]) {
      [arr[i], arr[i + 1]] = [arr[i + 1], arr[i]];
    }
  }

  // Recursive call for the remaining unsorted part
  recursiveBubbleSort(arr, n - 1);
}

let arr = [10, 5, 1, 12, 3, 44, 2, 4, 8];
console.log("Before sorting:", arr);

recursiveBubbleSort(arr, arr.length);

console.log("After sorting:", arr); // Output: [1, 2, 3, 4, 5, 8, 10, 12, 44]
```

## Optimized Approach ⚡

To optimize for the best case (already sorted array), add a flag to check if any swaps occurred. If no swaps, the array is sorted and recursion can stop early.

```javascript
function optimizedRecursiveBubbleSort(arr, n) {
  if (n == 1) return;

  let swapped = false;
  for (let i = 0; i < n - 1; i++) {
    if (arr[i] > arr[i + 1]) {
      [arr[i], arr[i + 1]] = [arr[i + 1], arr[i]];
      swapped = true;
    }
  }

  if (!swapped) return; // Array is already sorted

  optimizedRecursiveBubbleSort(arr, n - 1);
}

let arr2 = [1, 2, 3, 4, 5];
console.log("Before sorting:", arr2);

optimizedRecursiveBubbleSort(arr2, arr2.length);

console.log("After sorting:", arr2); // Output: [1, 2, 3, 4, 5]
```

## Summary 🎉

- Recursive Bubble Sort replaces loops with recursive calls.
- Each recursive call sorts the largest unsorted element to its correct position.
- Optimized version stops early if the array is already sorted, improving efficiency in the best case.