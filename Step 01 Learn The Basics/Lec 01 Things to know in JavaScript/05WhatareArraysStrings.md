# Lecture 01: What are Arrays and Strings in JavaScript

## Arrays

An array is a data structure that can hold multiple values in a single variable. Each value is called an element, and elements are accessed by their index (starting from 0).

### Example

```javascript
let numbers = [10, 20, 30, 40, 50];
console.log(numbers[0]); // Output: 10
console.log(numbers.length); // Output: 5
```

### Common Array Operations

- **Accessing elements:** `array[index]`
- **Adding elements:** `array.push(value)`
- **Removing elements:** `array.pop()`
- **Iterating:**  
  ```javascript
  for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);
  }
  ```

## Strings

A string is a sequence of characters used to represent text.

### Example

```javascript
let name = "Sambhav";
console.log(name[0]); // Output: S
console.log(name.length); // Output: 7
```

### Common String Operations

- **Concatenation:** `let fullName = "John" + " Doe";`
- **Accessing characters:** `string[index]`
- **Changing case:**  
  ```javascript
  console.log(name.toUpperCase()); // Output: SAMBHAV
  console.log(name.toLowerCase()); // Output: sambhav
  ```
- **Substring:**  
  ```javascript
  console.log(name.substring(0, 3)); // Output: Sam
  ```

## Summary

- Arrays store multiple values; strings store sequences of characters.
- Both arrays and strings have built-in methods for manipulation and access.