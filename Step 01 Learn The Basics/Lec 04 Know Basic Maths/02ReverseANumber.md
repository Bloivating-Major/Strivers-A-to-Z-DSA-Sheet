# Lecture 04: Reverse a Number in JavaScript 🔄

Reversing a number is a classic programming challenge! It’s useful for palindromes, number manipulation, and just for fun. Let’s explore creative ways to reverse a number in JavaScript.

## Approach 1: Using a Loop 🌀

Extract digits one by one and build the reversed number.

```javascript
function reverseNumber(num) {
  let reversed = 0;
  let n = Math.abs(num); // Handle negative numbers
  while (n > 0) {
    let digit = n % 10;
    reversed = reversed * 10 + digit;
    n = Math.floor(n / 10);
  }
  // Preserve the sign of the original number
  return num < 0 ? -reversed : reversed;
}

console.log(reverseNumber(12345)); // Output: 54321
console.log(reverseNumber(-987));  // Output: -789
console.log(reverseNumber(1000));  // Output: 1
```

## Approach 2: Using String Methods 🎨

Convert the number to a string, reverse it, and convert back to a number.

```javascript
function reverseNumber(num) {
  const str = Math.abs(num).toString().split('').reverse().join('');
  const reversed = parseInt(str, 10);
  return num < 0 ? -reversed : reversed;
}

console.log(reverseNumber(12345)); // Output: 54321
console.log(reverseNumber(-987));  // Output: -789
console.log(reverseNumber(1000));  // Output: 1
```

## Fun Fact 💡

Reversing numbers is a key step in checking if a number is a palindrome!

## Summary 🎉

- **Loop Approach:** Extract digits and build the reversed number.
- **String Approach:** Convert to string, reverse, and convert back.
- Both methods handle negative numbers and leading zeros effectively.