# Lecture 01: Move Zeroes to End of Array 🔢➡️

Moving all zeroes to the end of an array while maintaining the order of non-zero elements is a common array manipulation problem. There are multiple approaches, from brute force to optimal solutions.

## Problem Statement 🤔

- Given an array, move all zeroes to the end while keeping the order of non-zero elements.
- Example: `[1, 0, 2, 3, 2, 0, 0]` → `[1, 2, 3, 2, 0, 0, 0]`

---

## Brute Force Approach 🐢

- Create a temporary array to store non-zero elements.
- Copy non-zero elements back to the original array.
- Fill the remaining positions with zeroes.

```javascript
let nums = [1, 0 , 2, 3, 2, 0, 0];
console.log("Before:", nums);

let temp = [];
let n = nums.length;

for(let i = 0; i < n; i++){
    if(nums[i] !== 0){
        temp.push(nums[i]);
    }
}

for(let i = 0; i < temp.length; i++){
    nums[i] = temp[i];
}

for(let i = temp.length; i < n; i++){
    nums[i] = 0;
}

console.log("After:", nums); // Output: [1, 2, 3, 2, 0, 0, 0]
```



## Summary 🎉

- Brute force uses extra space and multiple passes.
