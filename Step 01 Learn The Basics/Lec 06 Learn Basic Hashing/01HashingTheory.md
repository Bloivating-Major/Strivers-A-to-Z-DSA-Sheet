# Lecture 06: Hashing Theory in JavaScript 🗝️🔢

Hashing is a technique used to map data of arbitrary size to fixed-size values. It's widely used in programming for fast data retrieval, searching, and storage.

## What is Hashing? 🤔

- Hashing uses a **hash function** to convert input (like a string or number) into a unique hash code (usually a number).
- The hash code is used as an index to store and retrieve data quickly in a data structure called a **hash table**.

## Why Use Hashing? 🚀

- **Fast lookups:** Access data in constant time, O(1), on average.
- **Efficient storage:** Store large amounts of data with minimal collisions.
- **Applications:** Used in dictionaries, caches, databases, and more.

## Hash Table Structure 🗂️

- Stores key-value pairs.
- Uses the hash function to determine where to store each key.
- Handles collisions (when two keys hash to the same index) using techniques like chaining or open addressing.

## Example in JavaScript 💻

```javascript
// Using JavaScript's built-in Map (a hash table)
let hashTable = new Map();
hashTable.set("apple", 1);
hashTable.set("banana", 2);

console.log(hashTable.get("apple")); // Output: 1
console.log(hashTable.has("banana")); // Output: true
```

## Common Hashing Applications 🌟

- Checking for duplicates in arrays
- Counting frequency of elements
- Implementing sets and maps
- Password storage (with cryptographic hash functions)

## Summary 🎉

- Hashing is a powerful tool for fast data access and management.
- Hash tables use hash functions to store and retrieve key-value pairs efficiently.
- JavaScript provides built-in support for hashing with `Map` and `Set`.