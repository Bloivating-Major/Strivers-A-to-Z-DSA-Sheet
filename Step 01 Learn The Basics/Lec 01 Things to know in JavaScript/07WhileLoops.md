# Lecture 01: While Loops in JavaScript 🔄

Loops are the heartbeat of programming! The `while` loop is a flexible way to repeat code as long as a condition stays true. It's perfect for situations where you don't know in advance how many times you'll need to loop.

## What is a While Loop? 🤔

A `while` loop keeps running as long as its condition is true. If the condition is false at the start, the loop won't run at all!

## Basic Syntax 📝

```javascript
while (condition) {
  // code to execute as long as condition is true
}
```

- **Condition:** The loop checks this before every iteration.
- **Body:** Runs only if the condition is true.

## Example: Counting Down 🚦

```javascript
let count = 5;
while (count > 0) {
  console.log("Countdown:", count);
  count--;
}
// Output: 5 4 3 2 1
```

## Example: User Input Loop 🎮

```javascript
let answer;
while (answer !== "yes") {
  answer = prompt("Type 'yes' to continue:");
}
console.log("You typed yes!");
```

## Creative Use: Generating Fibonacci Numbers 🐇

```javascript
let a = 0, b = 1;
let n = 7;
let i = 1;
console.log(a); // 0
while (i < n) {
  console.log(b); // 1, 1, 2, 3, 5, 8, ...
  let next = a + b;
  a = b;
  b = next;
  i++;
}
```

## Tips & Tricks 💡

- Make sure your condition will eventually become false, or you'll create an infinite loop! 🔁
- Use `while` when you don't know how many times you'll need to repeat.
- You can use `break` to exit the loop early.

## When to Use While Loops? 🚦

- When the number of iterations isn't known in advance.
- When waiting for user input or a specific event.
- When processing data until a condition is met.

## Summary 🎉

The `while` loop is a versatile tool for repeating actions in JavaScript. Use it wisely to control the flow of your programs and handle dynamic situations effectively!