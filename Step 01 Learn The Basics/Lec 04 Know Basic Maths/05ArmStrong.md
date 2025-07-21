# Lecture 04: Armstrong Number in JavaScript 💡

An Armstrong number (also called a narcissistic number) is a number that is equal to the sum of its own digits each raised to the power of the number of digits. For example, 153 is an Armstrong number because:  
1³ + 5³ + 3³ = 1 + 125 + 27 = 153

## How to Check for Armstrong Number in JavaScript

### Step-by-Step Approach

1. Count the number of digits in the number.
2. For each digit, raise it to the power of the total number of digits and sum the results.
3. If the sum equals the original number, it's an Armstrong number!

### Example Code

```javascript
function isArmstrong(num) {
  const digits = Math.abs(num).toString().split('');
  const power = digits.length;
  let sum = 0;

  for (let digit of digits) {
    sum += Math.pow(Number(digit), power);
  }

  return sum === Math.abs(num);
}

console.log(isArmstrong(153)); // Output: true
console.log(isArmstrong(370)); // Output: true
console.log(isArmstrong(9474)); // Output: true
console.log(isArmstrong(123)); // Output: false
```

## Fun Fact 💡

All single-digit numbers are Armstrong numbers!

## Summary 🎉

- An Armstrong number is equal to the sum of its digits each raised to the power of the number of digits.
- Use loops and Math.pow to check for Armstrong numbers in JavaScript.