# Lecture 05: Understand Recursion by Printing Something N Times 🔁

Recursion is a technique where a function calls itself to solve a problem. It's a fundamental concept in programming and is especially useful for problems that can be broken down into smaller, similar subproblems.

## What is Recursion? 🤔

- A recursive function calls itself with a modified argument.
- Every recursive function needs a **base case** to stop the recursion.

## Example: Print "Hello" N Times Using Recursion

Let's print "Hello" N times using recursion:

```javascript
function printHello(n) {
  if (n === 0) return; // Base case: stop when n reaches 0
  console.log("Hello");
  printHello(n - 1); // Recursive call with n-1
}

printHello(5);
// Output:
// Hello
// Hello
// Hello
// Hello
// Hello
```

## How It Works 🛠️

1. The function prints "Hello" and calls itself with `n-1`.
2. This repeats until `n` becomes 0, which is the base case.
3. The recursion unwinds and stops.

## Why Use Recursion? 🌱

- Simplifies code for problems that have repetitive, self-similar structure.
- Useful for tasks like traversing trees, solving mathematical problems, and more.

## Summary 🎉

- Recursion is calling a function within itself.
- Always define a base case to prevent infinite loops.
- Printing something N times is a classic way to understand recursion.