# Lecture 01: Maximum Consecutive Ones in an Array 🔥➕1️⃣

Finding the maximum number of consecutive 1s in a binary array is a common array problem. The goal is to scan the array and count the longest streak of 1s.

## Problem Statement 🤔

- Given a binary array, find the maximum number of consecutive 1s.
- Example: `[1, 1, 0, 1, 1, 1]` → Output: `3`

---

## Approach 🚀

- Use two variables: `count` to track the current streak of 1s, and `max` to store the maximum streak found so far.
- Traverse the array:
  - If the current element is 1, increment `count` and update `max` if needed.
  - If the current element is 0, reset `count` to 0.

## Code Implementation 💻

```javascript
var findMaxConsecutiveOnes = function(nums) {
    let count = 0; 
    let max = 0;
    for(let i = 0; i < nums.length; i++){
        if(nums[i] === 1) {
            count++;
            max = Math.max(count, max);    
        }
        else count = 0;
    }
    return max;
};
```

---

## Time Complexity ⏳

- **O(n)** — Traverse the array once.

## Space Complexity 🧠

- **O(1)** — Only uses a few variables for counting.

---

## Summary 🎉

- Efficiently finds the longest streak of 1s in a binary array.
- Uses a single pass and constant space.
- Useful for problems involving binary data analysis.