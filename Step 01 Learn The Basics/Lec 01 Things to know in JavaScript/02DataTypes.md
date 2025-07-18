# Lecture 01: Data Types in JavaScript

JavaScript has several built-in data types. Understanding these is essential for working with variables and functions.

## Primitive Data Types

1. **Number**  
   Represents both integer and floating-point numbers.  
   Example:
   ```javascript
   let age = 25;
   let price = 99.99;
   ```

2. **String**  
   Represents textual data.  
   Example:
   ```javascript
   let name = "Sambhav";
   ```

3. **Boolean**  
   Represents true or false values.  
   Example:
   ```javascript
   let isActive = true;
   ```

4. **Undefined**  
   A variable that has been declared but not assigned a value.  
   Example:
   ```javascript
   let x;
   console.log(x); // undefined
   ```

5. **Null**  
   Represents an intentional absence of value.  
   Example:
   ```javascript
   let y = null;
   ```

6. **Symbol**  
   Used for unique identifiers (advanced usage).

## Non-Primitive Data Types

1. **Object**  
   Used to store collections of data and more complex entities.  
   Example:
   ```javascript
   let person = {
     name: "Sambhav",
     age: 25
   };
   ```

2. **Array**  
   Special type of object for ordered collections.  
   Example:
   ```javascript
   let numbers = [1, 2, 3, 4, 5];
   ```

---