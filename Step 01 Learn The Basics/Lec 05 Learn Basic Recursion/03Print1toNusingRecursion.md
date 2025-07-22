# Lecture 05: Print 1 to N Using Recursion 🔢

Recursion is a powerful tool for solving problems that can be broken down into smaller, similar subproblems. Printing numbers from 1 to N using recursion is a classic way to understand how recursive calls work!

## What is Recursion? 🤔

- A recursive function calls itself with a modified argument.
- Every recursive function must have a **base case** to stop the recursion.

## Example: Print Numbers from 1 to N

Let's print numbers from 1 to N using recursion:

```javascript
function print1toN(n, current = 1) {
  if (current > n) return; // Base case: stop when current exceeds n
  console.log(current);
  print1toN(n, current + 1); // Recursive call with current + 1
}

print1toN(5);
// Output:
// 1
// 2
// 3
// 4
// 5
```

## How Does It Work? 🛠️

1. The function prints the current number.
2. It calls itself with the next number (`current + 1`).
3. This repeats until `current` exceeds `n`, which is the base case.
4. The recursion unwinds and stops.

## Alternative Approach: Using Only N

You can also use a slightly different approach by printing after the recursive call:

```javascript
function print1toN(n) {
  if (n === 0) return;
  print1toN(n - 1);
  console.log(n);
}

print1toN(5);
// Output:
// 1
// 2
// 3
// 4
// 5
```

## Why Learn This? 🌱

- Recursion simplifies code for problems with repetitive structure.
- It's essential for algorithms, tree traversals, and mathematical problems.

## Summary 🎉

- Recursion is calling a function within itself.
- Always define a base case to prevent infinite loops.
- Printing 1 to N is a classic way to master recursion!