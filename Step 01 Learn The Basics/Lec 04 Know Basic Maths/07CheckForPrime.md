# Lecture 04: Check for Prime Number in JavaScript 🔍

A prime number is a number greater than 1 that has no divisors other than 1 and itself. Checking for primes is a classic problem in programming and mathematics!

## Approach 1: Simple Loop

Check if the number is divisible by any number from 2 up to n-1.

```javascript
function isPrime(num) {
  if (num <= 1) return false;
  for (let i = 2; i < num; i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
}

console.log(isPrime(7));  // Output: true
console.log(isPrime(10)); // Output: false
console.log(isPrime(1));  // Output: false
```

## Approach 2: Efficient Approach (Up to √n)

You only need to check divisibility up to the square root of the number for efficiency.

```javascript
function isPrime(num) {
  if (num <= 1) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
}

console.log(isPrime(13)); // Output: true
console.log(isPrime(25)); // Output: false
```

## Fun Fact 💡

2 is the smallest and only even prime number!

## Summary 🎉

- A prime number has exactly two divisors: 1 and itself.
- Use the efficient approach for larger numbers to reduce time complexity.