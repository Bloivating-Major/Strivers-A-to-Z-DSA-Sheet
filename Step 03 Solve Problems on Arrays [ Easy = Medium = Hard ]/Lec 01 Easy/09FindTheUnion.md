# Lecture 01: Find the Union of Two Sorted Arrays 🔗🔢

Finding the union of two sorted arrays (which may contain duplicates) is a common problem in coding interviews. The union should contain all unique elements from both arrays, in sorted order.

## Problem Statement 🤔

- Given two sorted arrays, find their union (all unique elements from both arrays).
- Example:  
  `arr1 = [1, 2, 2, 3, 4]`  
  `arr2 = [2, 3, 4, 5, 6]`  
  **Union:** `[1, 2, 3, 4, 5, 6]`

---

## Brute Force Approach 🐢

- Add all elements from both arrays to a Set (removes duplicates).
- Convert the Set back to an array.

```javascript
let arr1 = [1, 2, 2, 3, 4];
let arr2 = [2, 3, 4, 5, 6];
let union = [];

let set = new Set();

for (let i = 0; i < arr1.length; i++) {
    set.add(arr1[i]);
}

for (let i = 0; i < arr2.length; i++) {
    set.add(arr2[i]);
}

for (let item of set) {
    union.push(item);
}
console.log(union); // Output: [1, 2, 3, 4, 5, 6]
```

**Time Complexity:** O(n1 + n2)  
**Space Complexity:** O(n1 + n2) (for the Set and union array)

---



## Summary 🎉

- Brute force uses a Set to remove duplicates.
