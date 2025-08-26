# Lecture 05: Fibonacci Number Using Recursion 🐚🔢

The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones. It starts with 0 and 1.  
Example: `0, 1, 1, 2, 3, 5, 8, 13, ...`

## What is the Fibonacci Sequence? 🤔

- **Definition:**  
  `fib(n) = fib(n-1) + fib(n-2)`
- **Base Cases:**  
  `fib(0) = 0`  
  `fib(1) = 1`

## Recursive Approach 🔁

- If `n` is 0 or 1, return `n` (base case).
- Otherwise, return `fib(n-1) + fib(n-2)`.

## Step-by-Step Algorithm 📝

1. If `n` is 0 or 1, return `n`.
2. Otherwise, recursively calculate `fib(n-1)` and `fib(n-2)`.
3. Add the results and return.

## Example Code 💻

```javascript
function fibonacci(n) {
  if (n === 0) return 0; // Base case
  if (n === 1) return 1; // Base case
  return fibonacci(n - 1) + fibonacci(n - 2); // Recursive case
}

console.log(fibonacci(0)); // Output: 0
console.log(fibonacci(1)); // Output: 1
console.log(fibonacci(5)); // Output: 5
console.log(fibonacci(7)); // Output: 13
```

## How Does It Work? 🛠️

- The function keeps calling itself for smaller values of `n`.
- When it reaches the base cases, it starts returning values.
- The recursion unwinds, adding up the results.

## Fun Fact 💡

- The Fibonacci sequence appears in nature, art, and architecture!

## Summary 🎉

- Recursion is a simple way to generate Fibonacci numbers.
- Always define base cases to avoid infinite recursion.
- Fibonacci numbers are widely used in mathematics and computer science!

```js
function fibonacci(n){
  if(n === 0) return 0;
  if(n === 1) return 1;

  return fibonacci(n-1) + fibonacci(n-2);
}

console.log(fibonacci(5));
```
