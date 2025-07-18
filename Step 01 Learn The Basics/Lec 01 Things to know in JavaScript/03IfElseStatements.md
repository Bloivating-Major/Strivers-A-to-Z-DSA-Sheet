# Lecture 01: If-Else Statements in JavaScript

If-else statements are used to make decisions in your code based on conditions.

## Basic Syntax

```javascript
if (condition) {
  // code to execute if condition is true
} else {
  // code to execute if condition is false
}
```

## Example

```javascript
let age = 18;

if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

## Else If Ladder

You can check multiple conditions using `else if`:

```javascript
let score = 85;

if (score >= 90) {
  console.log("Grade: A");
} else if (score >= 80) {
  console.log("Grade: B");
} else if (score >= 70) {
  console.log("Grade: C");
} else {
  console.log("Grade: D");
}
```

---