# Lecture 01: Remove Duplicates from Sorted Array 🗑️🔢

Removing duplicates from a sorted array is a common interview question. The goal is to modify the array in-place so that each element appears only once and return the new length.

## Brute Force Approach 🐢

- Use a Set to collect unique values.
- Overwrite the original array with the unique values from the Set.
- Return the size of the Set as the new length.

```javascript
var removeDuplicates = function(nums) {
    let set = new Set();

    // Step 1: collect unique values
    for (let i = 0; i < nums.length; i++) {
        set.add(nums[i]);
    }

    // Step 2: overwrite back into nums
    let i = 0;
    for (let val of set) {
        nums[i] = val;
        i++;
    }

    return set.size;
};
```

## Summary 🎉

- Brute force uses extra space (Set), while the optimal solution works in-place.


## Time and Space Complexity ⏱️

- Brute Force:
  - Time Complexity: O(n)
  - Space Complexity: O(n)

