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

---

## Optimal Solution ⚡ (Two Pointer Approach)

- Find the first zero in the array.
- Use two pointers: one for the zero position (`j`), and one to scan ahead (`i`).
- Whenever a non-zero is found, swap it with the zero at position `j` and move `j` forward.

```javascript
let nums = [1, 0 , 2, 3, 2, 0, 0];

let j = -1;

for(let i = 0; i < nums.length; i++){
    if(nums[i] === 0){
        j = i;
        break;
    }
}

if(j === -1) console.log('All numbers are non-zero');

for(let i = j + 1; i < nums.length; i++){
    if(nums[i] !== 0){
        [nums[j], nums[i]] = [nums[i], nums[j]];
        j++;
    }
}

console.log(nums); // Output: [1, 2, 3, 2, 0, 0, 0]
```

---

## Summary 🎉

- Brute force uses extra space and multiple passes.
- Optimal solution uses two pointers for in-place rearrangement and is more efficient.
- Both methods maintain the order of non-zero elements.