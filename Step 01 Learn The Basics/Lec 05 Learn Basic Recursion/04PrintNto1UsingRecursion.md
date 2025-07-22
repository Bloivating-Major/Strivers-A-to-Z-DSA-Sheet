# Lecture 05: Print N to 1 Using Recursion 🔄

Recursion is a powerful technique for solving problems that can be broken down into smaller, similar subproblems. Printing numbers from N down to 1 using recursion is a classic example to understand how recursive calls work in reverse order!

## What is Recursion? 🤔

- A recursive function calls itself with a modified argument.
- Every recursive function must have a **base case** to stop the recursion and avoid infinite loops.

## Example: Print Numbers from N to 1

Let's print numbers from N down to 1 using recursion:

```javascript
function printNto1(n) {
  if (n === 0) return; // Base case: stop when n reaches 0
  console.log(n);
  printNto1(n - 1); // Recursive call with n-1
}

printNto1(5);
// Output:
// 5
// 4
// 3
// 2
// 1
```

## How Does It Work? 🛠️

1. The function prints the current number `n`.
2. It calls itself with `n-1`.
3. This repeats until `n` becomes 0 (the base case).
4. The recursion unwinds and stops.

## Alternative Approach: Using an Additional Parameter

You can also use an additional parameter to control the current value:

```javascript
function printNto1(n, current = n) {
  if (current === 0) return;
  console.log(current);
  printNto1(n, current - 1);
}

printNto1(5);
// Output:
// 5
// 4
// 3
// 2
// 1
```

## Why Learn This? 🌱

- Recursion helps simplify code for repetitive, self-similar problems.
- It's essential for algorithms, tree traversals, and mathematical computations.

## Summary 🎉

- Recursion is calling a function within itself.
- Always define a base case to prevent infinite loops.
- Printing N to 1 is a classic way to master recursion!