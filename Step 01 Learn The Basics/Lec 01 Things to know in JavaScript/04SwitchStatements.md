# Lecture 01: Switch Statements in JavaScript

Switch statements are used to execute different blocks of code based on the value of an expression. They are useful when you need to compare the same variable to multiple values.

## Basic Syntax

```javascript
switch (expression) {
  case value1:
    // code block
    break;
  case value2:
    // code block
    break;
  default:
    // code block
}
```

## Example

```javascript
let fruit = "apple";

switch (fruit) {
  case "banana":
    console.log("Banana is yellow.");
    break;
  case "apple":
    console.log("Apple is red.");
    break;
  case "orange":
    console.log("Orange is orange.");
    break;
  default:
    console.log("Unknown fruit.");
}
```

## How It Works

- The `switch` statement evaluates the expression.
- It compares the result to each `case` value.
- If a match is found, the corresponding code block runs.
- The `break` statement stops further checking.
- If no match is found, the `default` block runs.

## Notes

- If you omit `break`, execution continues to the next case (fall-through).
- You can use any expression as the switch value, including numbers and strings.