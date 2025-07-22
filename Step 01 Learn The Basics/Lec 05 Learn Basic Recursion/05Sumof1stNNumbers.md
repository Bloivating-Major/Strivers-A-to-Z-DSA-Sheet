# Lecture 05: Sum of First N Numbers Using Recursion ➕

Recursion is a powerful way to solve problems that can be broken down into smaller, similar subproblems. Calculating the sum of the first N natural numbers is a classic example to understand recursion in action!

## What is Recursion? 🤔

- A recursive function calls itself with a modified argument.
- Every recursive function must have a **base case** to stop the recursion.

## Example: Sum of First N Numbers

Let's calculate the sum of the first N numbers using recursion:

```javascript
function sumOfN(n) {
  if (n === 0) return 0; // Base case: sum of 0 is 0
  return n + sumOfN(n - 1); // Recursive call
}

console.log(sumOfN(5)); // Output: 15 (1+2+3+4+5)
console.log(sumOfN(10)); // Output: 55 (1+2+...+10)
```

## How Does It Work? 🛠️

1. The function adds `n` to the sum of numbers up to `n-1`.
2. This repeats until `n` becomes 0 (the base case).
3. The recursion unwinds, adding up all the numbers.

## Why Learn This? 🌱

- Recursion simplifies code for problems with repetitive structure.
- It's essential for algorithms, mathematical problems, and coding interviews.

## Summary 🎉

- Recursion is calling a function within itself.
- Always define a base case to prevent infinite loops.
- Calculating the sum of first N numbers is a classic way to master recursion!