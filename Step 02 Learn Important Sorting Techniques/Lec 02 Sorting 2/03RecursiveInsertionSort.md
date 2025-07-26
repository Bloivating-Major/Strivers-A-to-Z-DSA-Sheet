# Lecture 02: Recursive Insertion Sort in JavaScript 🔁📝

Insertion Sort can be implemented using recursion! Instead of using loops to process each element, we use recursive calls to sort the array step by step.

## Approach 🚀

1. **Recursive Selection:**  
   Call the recursive function with the array, its length, and the current index (`i`).
2. **Insert Element:**  
   Take the element at index `i` and place it in its correct position in the sorted part of the array (to its left).
3. **Shift Elements:**  
   Shift elements greater than the selected element to the right.
4. **Recursive Call:**  
   Call the function again with the next index (`i + 1`).
5. **Base Case:**  
   If `i == n`, stop recursion.

## Example Code 💻

```javascript
function recursiveInsertionSort(arr, n, i = 1) {
  // Base case: if all elements are covered
  if (i === n) return;

  let key = arr[i];
  let j = i - 1;

  // Move elements greater than key to one position ahead
  while (j >= 0 && arr[j] > key) {
    arr[j + 1] = arr[j];
    j--;
  }
  arr[j + 1] = key;

  // Recursive call for next index
  recursiveInsertionSort(arr, n, i + 1);
}

let arr = [13, 46, 24, 52, 20, 9];
console.log("Before sorting:", arr);

recursiveInsertionSort(arr, arr.length);

console.log("After sorting:", arr); // Output: [9, 13, 20, 24, 46, 52]
```

## How It Works 🛠️

- The function sorts the array up to the current index.
- Each recursive call inserts the next element into its correct position.
- Recursion continues until all elements are sorted.

## Summary 🎉

- Recursive Insertion Sort replaces loops with recursive calls.
- Each call places the selected element in its correct position.
- The base case ensures recursion stops when the entire array is sorted.