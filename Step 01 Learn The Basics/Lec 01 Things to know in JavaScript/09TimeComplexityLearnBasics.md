# Lecture 01: Time Complexity - Learn the Basics ⏳

Time complexity is a way to measure how the runtime of an algorithm grows as the input size increases. It helps you analyze and compare the efficiency of different solutions.

## Why Time Complexity Matters? 🤔

- Helps you write efficient code.
- Predicts how your program will scale with larger inputs.
- Essential for coding interviews and competitive programming.

## Big O Notation 🅾️

Big O notation describes the upper bound of an algorithm's running time. It focuses on the most significant factors as input size grows.

### Common Time Complexities

- **O(1):** Constant time  
  The algorithm takes the same time regardless of input size.
  ```javascript
  function printFirst(arr) {
    console.log(arr[0]);
  }
  ```
- **O(n):** Linear time  
  Time grows proportionally with input size.
  ```javascript
  function printAll(arr) {
    for (let i = 0; i < arr.length; i++) {
      console.log(arr[i]);
    }
  }
  ```
- **O(n²):** Quadratic time  
  Time grows with the square of the input size (nested loops).
  ```javascript
  function printPairs(arr) {
    for (let i = 0; i < arr.length; i++) {
      for (let j = 0; j < arr.length; j++) {
        console.log(arr[i], arr[j]);
      }
    }
  }
  ```

## Space Complexity 🧠

Space complexity measures how much extra memory your algorithm uses as input size grows.

- **O(1):** Uses a constant amount of space.
- **O(n):** Uses space proportional to input size.

## Tips & Tricks 💡

- Focus on the fastest-growing term (ignore constants and lower-order terms).
- Optimize loops and nested operations.
- Know the time complexity of built-in methods (e.g., `Array.push` is O(1), `Array.sort` is O(n log n)).

## Summary 🎉

- Time complexity helps you compare and optimize algorithms.
- Big O notation is the standard way to express complexity.
- Efficient code is crucial for performance, especially with large datasets.

## Common Time Complexity Notations in Big O

- **O(1): Constant Time**  
  The algorithm takes the same amount of time regardless of input size.

- **O(log n): Logarithmic Time**  
  Time increases logarithmically as input grows (e.g., binary search).

- **O(n): Linear Time**  
  Time increases proportionally with input size.

- **O(n log n): Linearithmic Time**  
  Common in efficient sorting algorithms like Merge Sort and Quick Sort.

- **O(n²): Quadratic Time**  
  Time increases with the square of the input size (e.g., nested loops).

- **O(n³): Cubic Time**  
  Time increases with the cube of the input size (e.g., triple nested loops).

- **O(2ⁿ): Exponential Time**  
  Time doubles with each additional input (e.g., recursive solutions to the subset problem).

- **O(n!): Factorial Time**  
  Time increases factorially with input size (e.g., brute-force permutations).

---

### Less Common Notations

- **O(√n): Square Root Time**  
  Used in some algorithms like trial division for prime checking.

- **O(log log n): Double Logarithmic Time**  
  Appears in some advanced data structures.

---

These notations help you analyze and compare the efficiency of algorithms as input size grows.