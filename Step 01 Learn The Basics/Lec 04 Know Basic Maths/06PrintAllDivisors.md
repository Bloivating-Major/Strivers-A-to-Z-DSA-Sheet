# Lecture 04: Print All Divisors of a Number in JavaScript 🧮

Finding all divisors of a number is a common math operation in programming. A divisor is a number that divides another number completely (with remainder 0).

## Approach 1: Simple Loop

Loop from 1 to the number and check if each value divides the number.

```javascript
function printDivisors(num) {
  for (let i = 1; i <= num; i++) {
    if (num % i === 0) {
      console.log(i);
    }
  }
}

printDivisors(12); // Output: 1 2 3 4 6 12
printDivisors(15); // Output: 1 3 5 15
```

## Approach 2: Efficient Approach (Up to √n)

You only need to loop up to the square root of the number. For each divisor found, you can also print its pair.

```javascript
function printDivisors(num) {
  for (let i = 1; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      console.log(i);
      if (i !== num / i) {
        console.log(num / i);
      }
    }
  }
}

printDivisors(36); // Output: 1 36 2 18 3 12 4 9 6
```

## Summary 🎉

- Divisors are numbers that divide the given number exactly.
- Use a simple loop for small numbers.
- Use the efficient approach for larger numbers to reduce time complexity.