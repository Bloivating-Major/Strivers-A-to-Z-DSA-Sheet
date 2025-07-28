# Lecture 01: Check If Array is Sorted and Rotated 🔄✅

Checking if an array is sorted and rotated is a common problem in coding interviews. The goal is to determine if the array can be rotated so that it becomes sorted in non-decreasing order.

## Problem Statement 🤔

- Given an array, check if it is sorted and rotated.
- An array is considered sorted and rotated if it is sorted in non-decreasing order and then rotated (shifted) some number of times.

## Approach 🚀

- Traverse the array and count the number of places where the current element is greater than the next element (considering circular rotation).
- If this count is 0, the array is already sorted.
- If the count is 1, the array is sorted and rotated.
- If the count is more than 1, the array is not sorted and rotated.

## Code Implementation 💻

```javascript
var check = function(nums) {
    let n = nums.length;
    let count = 0;

    for(let i = 0; i < n; i++){
        if(nums[i] > nums[(i+1) % n]){
            count++;
        }
    }

    return count <= 1;
};
```

## Example 🌟

```javascript
console.log(check([3, 4, 5, 1, 2])); // Output: true (sorted and rotated)
console.log(check([1, 2, 3, 4, 5])); // Output: true (already sorted)
console.log(check([2, 1, 3, 4, 5])); // Output: false (not sorted and rotated)
```

## Summary 🎉

- Count the number of "drops" in the array.
- If the count is 0 or 1, the array is sorted and rotated.
- Efficient solution with O(n) time complexity and O(1) space complexity.