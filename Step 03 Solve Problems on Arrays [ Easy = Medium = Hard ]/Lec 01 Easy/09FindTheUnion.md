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

## Optimal Approach ⚡ (Two Pointer Technique)

- Use two pointers to traverse both arrays.
- Add the smaller element to the union array, skipping duplicates.
- Continue until both arrays are fully traversed.

```javascript
let arr1 = [1, 2, 2, 3, 4];
let arr2 = [2, 3, 4, 5, 6];
let union = [];

let n1 = arr1.length;
let n2 = arr2.length;
let i = 0, j = 0;

while(i < n1 && j < n2){
    if(arr1[i] <= arr2[j]){
        if(union.length === 0 || union[union.length-1] !== arr1[i]){
            union.push(arr1[i]);
        }
        i++;
    }else{
        if(union.length === 0 || union[union.length-1] !== arr2[j]){
            union.push(arr2[j]);
        }
        j++;
    }
}

while(i < n1){
    if(union[union.length-1] !== arr1[i]){
        union.push(arr1[i]);
    }
    i++;
}

while(j < n2){
    if(union[union.length-1] !== arr2[j]){
        union.push(arr2[j]);
    }
    j++;
}

console.log(union); // Output: [1, 2, 3, 4, 5, 6]
```

**Time Complexity:** O(n1 + n2)  
**Space Complexity:** O(n1 + n2) (for the union array)

---

## Summary 🎉

- Brute force uses a Set to remove duplicates.
- Optimal approach uses two pointers for efficient traversal and duplicate removal.
- Both methods have O(n1 + n2) time and space complexity.
- Always prefer the optimal approach for interviews and large datasets.