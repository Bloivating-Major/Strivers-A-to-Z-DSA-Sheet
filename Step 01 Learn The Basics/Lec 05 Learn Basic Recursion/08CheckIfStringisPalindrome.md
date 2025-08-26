# Lecture 05: Check If a String is a Palindrome Using Recursion 🔁✨

A palindrome is a string that reads the same forwards and backwards, like "madam" or "racecar". Checking for palindromes is a classic problem in programming!

## What is a Palindrome? 🤔

- A string is a palindrome if the first and last characters are the same, and the substring between them is also a palindrome.
- Example:  
  `"level"` → palindrome  
  `"hello"` → not a palindrome

## Recursive Approach 🔁

- Compare the first and last characters.
- If they match, recursively check the substring between them.
- Stop when the start index is greater than or equal to the end index (base case).

## Step-by-Step Algorithm 📝

1. Define a function that takes the string, a start index, and an end index.
2. If `start >= end`, return `true` (base case).
3. If `str[start] !== str[end]`, return `false`.
4. Recursively check the substring from `start + 1` to `end - 1`.

## Example Code 💻

```javascript
function isPalindrome(str, start = 0, end = str.length - 1) {
  if (start >= end) return true; // Base case
  if (str[start] !== str[end]) return false;
  return isPalindrome(str, start + 1, end - 1);
}

console.log(isPalindrome("madam"));    // Output: true
console.log(isPalindrome("racecar"));  // Output: true
console.log(isPalindrome("hello"));    // Output: false
console.log(isPalindrome("a"));        // Output: true
```

## How Does It Work? 🛠️

- The function compares the outer characters and moves inward.
- Each recursive call checks a smaller substring.
- When the indices meet or cross, recursion stops!

## Creative Twist: Try with Emojis or Phrases 🎨

```javascript
console.log(isPalindrome("😀🐱🍕🐱😀")); // Output: true
```

## Summary 🎉

- Recursion is a neat way to check for palindromes.
- Always set a base case to avoid infinite recursion.
- Works for strings, phrases, and even emojis!

```js
// Revision Session 

let s = "A man, a plan, a canal: Panama";

s = s.toLowerCase().replace(/[^a-z0-9]/g, '');

function check(s, left, right){
    if(left >= right) return true;
    
    if(s[left] !== s[right]) return false;
    
    return check(s, left+1, right-1);
}

let ans = check(s, 0, s.length-1);

console.log(ans);
```

Revision Done.