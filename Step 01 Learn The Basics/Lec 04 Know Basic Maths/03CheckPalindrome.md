# Lecture 04: Check if a Number is a Palindrome in JavaScript 🔁

A palindrome is a number that reads the same forwards and backwards, like 121 or 1331. Checking for palindromes is a common programming challenge!

## Approach 1: Reverse and Compare 🔄

Reverse the number and check if it matches the original.

```javascript
function isPalindrome(num) {
  const original = Math.abs(num);
  let reversed = 0, n = original;
  while (n > 0) {
    reversed = reversed * 10 + (n % 10);
    n = Math.floor(n / 10);
  }
  return original === reversed;
}

console.log(isPalindrome(121));   // Output: true
console.log(isPalindrome(1331));  // Output: true
console.log(isPalindrome(123));   // Output: false
console.log(isPalindrome(-121));  // Output: true (ignores sign)
```

## Approach 2: Using String Methods 🎨

Convert the number to a string, reverse it, and compare.

```javascript
function isPalindrome(num) {
  const str = Math.abs(num).toString();
  const reversedStr = str.split('').reverse().join('');
  return str === reversedStr;
}

console.log(isPalindrome(1221));  // Output: true
console.log(isPalindrome(1234));  // Output: false
```

## Fun Fact 💡

Palindromes aren’t just for numbers—they’re also found in words like "madam" and "racecar"!

## Summary 🎉

- **Reverse and Compare:** Reverse the digits and check equality.
- **String Approach:** Convert to string, reverse, and compare.
- Both methods work for positive and negative numbers (ignoring the sign).