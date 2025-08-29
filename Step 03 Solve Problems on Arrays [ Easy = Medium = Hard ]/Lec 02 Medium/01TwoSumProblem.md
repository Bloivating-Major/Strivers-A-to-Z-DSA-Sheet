# Lecture 01: Longest Subarray with Sum K 🧮➕

Finding the longest subarray with a given sum K is a classic array problem. The goal is to find the maximum length of a contiguous subarray whose elements sum up to K. This problem can be solved using brute force, better, and optimal approaches.

---

## Problem Statement 🤔

- Given an array and an integer K, find the length of the longest subarray whose sum is exactly K.
- Example:  
  If `arr = [1, 2, 3, 1, 1, 1, 4, 5, 3]` and `K = 3`,  
  possible subarrays are `[1, 2]`, `[3]`, `[1, 1, 1]`, etc.  
  The answer is `3` (for `[1, 1, 1]`).

---

## Brute Force Approach 🐢

- Check all possible subarrays.
- For each subarray, calculate the sum and update the maximum length if the sum equals K.

```javascript
let length = 0;
for(let i = 0; i < arr.length; i++){
    let sum = 0;
    for(let j = i; j < arr.length; j++){
        sum += arr[j];
        if(sum === K) length = Math.max(length, j - i + 1);
    }
}
console.log(length);
```
**Time Complexity:** O(n²)  
**Space Complexity:** O(1)

---

## Better Solution ⚡ (Using Hash Map)

- Use a map to store the prefix sum and its earliest index.
- For each index, check if (current sum - K) exists in the map.
- If yes, update the maximum length.

```javascript
let map = new Map();
let sum = 0;
let length = 0;
map.set(0, -1); // To handle subarrays starting from index 0

for(let i = 0; i < arr.length; i++){
    sum += arr[i];
    if(map.has(sum - K)){
        length = Math.max(length, i - map.get(sum - K));
    }
    if(!map.has(sum)){
        map.set(sum, i);
    }
}
console.log(length);
```
**Time Complexity:** O(n)  
**Space Complexity:** O(n)

---

## Optimal Solution 🚀 (Sliding Window, for Positive Numbers Only)

- Use two pointers (`left` and `right`) and a running sum.
- Expand the window by moving `right` and add elements to the sum.
- If the sum exceeds K, shrink the window from the left.
- Update the maximum length when the sum equals K.

```javascript
let left = 0, right = 0, sum = arr[0], length = 0;

while(right < arr.length){
    while(left <= right && sum > K){
        sum -= arr[left];
        left++;
    }
    if(sum === K){
        length = Math.max(length, right - left + 1);
    }
    right++;
    if(right < arr.length){
        sum += arr[right];
    }
}
console.log(length);
```
**Time Complexity:** O(n)  
**Space Complexity:** O(1)

---

## Summary 🎉

- Brute force checks all subarrays (O(n²)), not efficient for large arrays.
- Hash map approach works for all integers and is efficient (O(n) time, O(n) space).
- Sliding window is optimal for positive numbers (O(n) time, O(1) space).
- Always choose the optimal approach for interviews and large datasets!