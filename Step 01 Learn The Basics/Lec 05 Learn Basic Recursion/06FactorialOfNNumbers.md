# Lecture 05: Factorial of N Numbers Using Recursion ✨

The factorial of a number N (`N!`) is the product of all natural numbers from 1 to N. It's a classic example to understand recursion in programming!

## What is Factorial? 🤔

- **Definition:**  
  `factorial(N) = N × (N-1) × (N-2) × ... × 1`
- **Special Case:**  
  By definition, `0! = 1`

## Recursive Approach 🔁

Recursion breaks the problem into smaller subproblems:

- **Recursive Formula:**  
  `factorial(N) = N × factorial(N - 1)`
- **Base Case:**  
  If `N == 0`, return `1`

## Step-by-Step Algorithm 📝

1. If `N` is 0, return 1 (base case).
2. Otherwise, multiply `N` by the factorial of `N-1`.
3. Repeat until you reach the base case.
4. The final result is the factorial of N!

## Example Code 💻

```javascript
// Recursive function to calculate factorial of a number
function factorial(n) {
  // Base case: factorial of 0 is 1
  if (n === 0) {
    return 1;
  }
  // Recursive case: n * factorial of (n-1)
  return n * factorial(n - 1);
}

// Define the number to compute factorial
const n = 3;

// Call the factorial function and print the result
console.log(factorial(n)); // Output: 6
```

## How Does It Work? 🛠️

- The function keeps calling itself with `n-1`.
- When `n` reaches 0, it returns 1.
- Each recursive call multiplies the result, building up the final answer.

## Fun Fact 💡

- Factorials grow very fast!  
  For example, `5! = 120`, `10! = 3,628,800`

## Summary 🎉

- Recursion is a powerful way to compute factorials.
- Always define a base case to avoid infinite loops.
- Factorials are widely used in mathematics, probability, and computer science!