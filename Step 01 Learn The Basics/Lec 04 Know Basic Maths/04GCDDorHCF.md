# Lecture 04: GCD (Greatest Common Divisor) or HCF (Highest Common Factor) in JavaScript 🧮

GCD (also called HCF) is the largest number that divides two numbers without leaving a remainder. It’s a fundamental concept in mathematics and programming!

## Approach 1: Euclidean Algorithm ⚡

The Euclidean algorithm is an efficient way to find the GCD of two numbers.

```javascript
function gcd(a, b) {
  while (b !== 0) {
    let temp = b;
    b = a % b;
    a = temp;
  }
  return Math.abs(a); // Handles negative numbers
}

console.log(gcd(24, 36)); // Output: 12
console.log(gcd(100, 85)); // Output: 5
console.log(gcd(-42, 56)); // Output: 14
```

## Approach 2: Recursive Euclidean Algorithm 🔁

You can also implement the Euclidean algorithm recursively.

```javascript
function gcd(a, b) {
  if (b === 0) return Math.abs(a);
  return gcd(b, a % b);
}

console.log(gcd(24, 36)); // Output: 12
console.log(gcd(100, 85)); // Output: 5
```

## Fun Fact 💡

GCD is used in simplifying fractions, cryptography, and finding LCM (Least Common Multiple)!

## Summary 🎉

- **GCD/HCF** is the largest number that divides two numbers exactly.
- The Euclidean algorithm is the most efficient way to compute GCD.
- Works for both positive and negative integers.