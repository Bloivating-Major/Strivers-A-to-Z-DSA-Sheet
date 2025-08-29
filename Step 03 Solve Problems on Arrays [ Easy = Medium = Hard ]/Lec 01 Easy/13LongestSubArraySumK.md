# Lecture 01: Longest Subarray with Sum K 🧮➕

Finding the longest subarray with a given sum K is a classic array problem. The goal is to find the maximum length of a contiguous subarray whose elements sum up to K. This problem can be solved using brute force, better, and optimal approaches.

---

## Problem Statement 🤔

- Given an array and an integer K, find the length of the longest subarray whose sum is exactly K.
- Example:  
  `arr = [1, 2, 3, 1, 1, 1, 4, 5, 3]`, `K = 3`  
  **Output:** `3` (subarray `[1, 1, 1]` or `[3]`)

---

## Brute Force Approach 🐢

- Check all possible subarrays.
- For each subarray, calculate the sum and update the maximum length if the sum equals K.

```javascript
let length = 0;
for(let i = 0; i < n; i++){
    let sum = 0;
    for(let j = i; j < n; j++){
        sum += arr[j];
        if(sum === k) length = Math.max(j - i + 1, length);
    }
}
console.log(length);
```
**Time Complexity:** O(n²)  
**Space Complexity:** O(1)

---


## Summary 🎉

- Brute force checks all subarrays (O(n²)), not efficient for large arrays.
- Hash map approach works for all integers and is efficient (O(n) time, O(n) space).
- Sliding window is optimal for positive numbers (O(n) time, O(1) space).
- Always choose the optimal approach for interviews and large datasets!