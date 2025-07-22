# Lecture 05: Print Your Name N Times Using Recursion 🧑‍💻🔁

Recursion is a powerful concept in programming where a function calls itself to solve a problem. Let's make it fun by printing your name N times using recursion!

## What is Recursion? 🤔

- A recursive function solves a problem by breaking it into smaller, similar subproblems.
- Every recursive function must have a **base case** to stop the recursion and avoid infinite loops.

## Example: Print Your Name N Times

Let's say you want to print your name (e.g., "Sambhav") 5 times using recursion.

```javascript
function printName(n) {
  if (n === 0) return; // Base case: stop when n reaches 0
  console.log("Sambhav");
  printName(n - 1); // Recursive call with n-1
}

printName(5);
// Output:
// Sambhav
// Sambhav
// Sambhav
// Sambhav
// Sambhav
```

## How Does It Work? 🛠️

1. The function prints your name and calls itself with `n-1`.
2. This repeats until `n` becomes 0 (the base case).
3. The recursion unwinds and stops, having printed your name N times.

## Creative Twist: Print with Numbering 🎨

You can make it more creative by printing the count along with your name!

```javascript
function printName(n, i = 1) {
  if (n === 0) return;
  console.log(i + ". Sambhav");
  printName(n - 1, i + 1);
}

printName(5);
// Output:
// 1. Sambhav
// 2. Sambhav
// 3. Sambhav
// 4. Sambhav
// 5. Sambhav
```

## Why Learn This? 🌱

- Recursion helps you solve problems with repetitive, self-similar structure.
- It's a key concept for algorithms, tree traversals, and mathematical problems.

## Summary 🎉

- Recursion is calling a function within itself.
- Always define a base case to prevent infinite loops.
- Printing your name N times is a fun way to master recursion!