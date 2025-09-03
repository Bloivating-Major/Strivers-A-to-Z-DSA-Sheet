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

## Better Approach ⚡

- Use a Map to count the frequency of each element.
- Return the element with a count of 1.

```javascript
let map = new Map();

for (let num of nums) {
    map.set(num, (map.get(num) || 0) + 1);
}

let single = -1;
for (let [key, val] of map) {
    if (val === 1) {
        single = key;
        break;
    }
}

return single;
```
**Time Complexity:** O(n)  
**Space Complexity:** O(n)

---

## Optimal Solution 🏅 (Using XOR)

- XOR all elements together. Pairs cancel out, leaving the single number.

```javascript
let single = 0;

for(let num of nums){
    single ^= num;
}

return single;
```
**Time Complexity:** O(n)  
**Space Complexity:** O(1)

---

## Summary 🎉

- Brute force checks each element's frequency, but is slow.
- Map-based solution is faster but uses extra space.
- XOR method is optimal: O(n) time and O(1) space.
- Always prefer the optimal approach for interviews and large datasets.