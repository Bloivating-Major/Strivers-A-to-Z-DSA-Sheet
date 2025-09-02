# Lecture 01: Find the Single Number in an Array 🕵️‍♂️🔢

Finding the single number in an array where every element appears twice except one is a classic coding interview problem. The goal is to identify the unique element.

## Problem Statement 🤔

- Given an array of integers, every element appears twice except for one. Find that single one.
- Example: `[2, 2, 1]` → Output: `1`

---

## Brute Force Approach 🐢

- For each element, count its occurrences in the array.
- If the count is 1, return that element.

```javascript
for(let i = 0; i < nums.length; i++){
    let num = nums[i];
    let count = 0; 
    for(let j = 0; j < nums.length; j++){
        if(nums[j] === num) count++;
    }
    if(count === 1) return num;
}
```
**Time Complexity:** O(n²)  
**Space Complexity:** O(1)

---



## Summary 🎉

- Brute force checks each element's frequency, but is slow.
