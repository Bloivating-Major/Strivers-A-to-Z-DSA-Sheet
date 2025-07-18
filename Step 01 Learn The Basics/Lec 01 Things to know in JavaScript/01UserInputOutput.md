# Lecture 01: Things to Know in JavaScript

## Basic Input/Output in JavaScript

### Output

You can display output in JavaScript using:

- `console.log()`: Prints messages to the browser console.
- `alert()`: Shows a popup alert box.
- `document.write()`: Writes directly to the HTML document (not recommended for modern web apps).

```javascript
console.log("Hello, World!"); // Output to console
alert("Welcome to JavaScript!"); // Popup alert
document.write("This is written to the document."); // Writes to HTML
```

### Input

JavaScript gets user input using:

- `prompt()`: Shows a dialog box for user input.

```javascript
let name = prompt("Enter your name:");
console.log("Hello, " + name);
```

### Example: Adding Two Numbers

```javascript
let num1 = prompt("Enter first number:");
let num2 = prompt("Enter second number:");
let sum = Number(num1) + Number(num2);
console.log("Sum is: " + sum);
```

---