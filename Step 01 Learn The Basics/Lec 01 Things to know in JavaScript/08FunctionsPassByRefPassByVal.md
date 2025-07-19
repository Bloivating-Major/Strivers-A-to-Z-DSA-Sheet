# Lecture 01: Functions, Pass by Value & Pass by Reference in JavaScript 🧑‍💻

Functions are reusable blocks of code that perform specific tasks. They help organize code and avoid repetition.

## Declaring and Using Functions

```javascript
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Sambhav"); // Output: Hello, Sambhav!
```

## Pass by Value vs Pass by Reference

### Pass by Value

- **Primitive data types** (Number, String, Boolean, etc.) are passed by value.
- The function receives a copy of the variable, so changes inside the function do not affect the original value.

```javascript
function changeValue(x) {
  x = 10;
}

let num = 5;
changeValue(num);
console.log(num); // Output: 5 (unchanged)
```

### Pass by Reference

- **Objects and Arrays** are passed by reference.
- The function receives a reference to the original object/array, so changes inside the function affect the original.

```javascript
function changeArray(arr) {
  arr[0] = 99;
}

let numbers = [1, 2, 3];
changeArray(numbers);
console.log(numbers); // Output: [99, 2, 3]
```

## Why Does This Matter?

- Use pass by value for simple data types when you don't want the original to change.
- Use pass by reference for objects/arrays when you want to modify the original data.

## Summary

- Functions make code reusable and organized.
- Primitive types are passed by value (safe from changes).
- Objects/arrays are passed by reference (can be modified).