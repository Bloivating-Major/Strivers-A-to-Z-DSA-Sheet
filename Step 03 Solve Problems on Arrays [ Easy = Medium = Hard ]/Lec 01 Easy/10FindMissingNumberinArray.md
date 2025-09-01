# Lecture 01: Find the Missing Number in an Array ❓🔢

Finding the missing number in an array containing numbers from 1 to N (with one missing) is a classic interview question. There are several approaches, from brute force to optimal solutions.

## Problem Statement 🤔

- Given an array of size N-1 containing numbers from 1 to N, find the missing number.
- Example: `arr = [1, 2, 4, 5]`, `N = 5`  
  **Missing Number:** `3`

---

## Brute Force Approach 🐢

- For each number from 1 to N, check if it exists in the array.
- If not found, that's the missing number.

```javascript
let arr = [1,2,4,5];
let n = 5;

for(let i = 1; i <= n; i++){
    let flag = 0;
    for(let j = 0; j < arr.length; j++){
        if(arr[j] === i){
            flag = 1;
            break;
        }
    }
    if(flag === 0){
        console.log("Missing number is", i); // Output: 3
    }
}
```
**Time Complexity:** O(n²)  
**Space Complexity:** O(1)

---

## Better Solution ⚡

- Use a Map to mark the presence of each number.
- Traverse the array and update the map.
- The number not marked is the missing one.

```javascript
let arr = [1,2,4,5];
let n = 5;
let map = new Map();

for(let i = 1; i <= n; i++){
    map.set(i, 0);
}

for(let i = 0; i < arr.length; i++){
    if(map.has(arr[i])){
        map.set(arr[i], 1);
    }
}

for(let i = 1; i <= n; i++){
    if(map.get(i) === 0){
        console.log("Missing number is", i); // Output: 3
    }
}
```
**Time Complexity:** O(n)  
**Space Complexity:** O(n)

---

## Optimal Solution 🏅 (Using Summation)

- The sum of numbers from 1 to N is `(N * (N + 1)) / 2`.
- Subtract the sum of array elements from this total to get the missing number.

```javascript
let arr = [1,2,4,5];
let n = 5;

let sum = (n * (n + 1)) / 2;
let sum2 = 0;

for(let i = 0; i < arr.length; i++){
    sum2 += arr[i];
}

console.log("Missing number is", sum - sum2); // Output: 3
```
**Time Complexity:** O(n)  
**Space Complexity:** O(1)

--- 

## Summary 🎉

- Brute force checks each number, but is slow for large arrays.
- Map-based solution is faster but uses extra space.
- Summation method is optimal: O(n) time and O(1) space.
- Always prefer the optimal approach for interviews and large datasets.