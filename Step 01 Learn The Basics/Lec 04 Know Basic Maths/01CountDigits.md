# Lecture 04: Count Digits in a Number (JavaScript)

Counting the number of digits in a number is a basic math operation often used in programming. Here’s how you can do it in JavaScript:

## Approach 1: Using a Loop

We repeatedly divide the number by 10 and count how many times we can do this before the number becomes 0.

```javascript
function countDigits(num) {
  let count = 0;
  num = Math.abs(num); // Handle negative numbers
  if (num === 0) return 1; // Special case for 0
  while (num > 0) {
    count++;
    num = Math.floor(num / 10);
  }
  return count;
}

console.log(countDigits(12345)); // Output: 5
console.log(countDigits(-789));  // Output: 3
console.log(countDigits(0));     // Output: 1
```

## Approach 2: Using String Conversion

Convert the number to a string and count the length (excluding the minus sign if present).

```javascript
function countDigits(num) {
  return Math.abs(num).toString().length;
}

console.log(countDigits(12345)); // Output: 5
console.log(countDigits(-789));  // Output: 3
console.log(countDigits(0));     // Output: 1
```

## Summary

- **Loop Approach:** Divide by 10 until the number is 0, counting steps.
- **String Approach:** Convert to string and count characters.
- Both methods work for positive and negative integers, with special handling for 0.