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

## Optimal Solution ⚡

- Use two pointers to overwrite duplicates in-place.
- Traverse the array, and whenever a new unique element is found, move it to the next position.
- Return the length of the unique portion.

```javascript
var removeDuplicates = function(nums) {
    let j = 0; 
    for(let i = 1; i < nums.length; i++){
        if(nums[j] !== nums[i]) {
            nums[j+1] = nums[i];
            j++;
        }
    }
    return j+1;
};
```

## Summary 🎉

- Brute force uses extra space (Set), while the optimal solution works in-place.
- The optimal approach is efficient and preferred for interviews.
- Both methods return the new length of the array without duplicates.

## Time and Space Complexity ⏱️

- Brute Force:
  - Time Complexity: O(n)
  - Space Complexity: O(n)

- Optimal Solution:
  - Time Complexity: O(n)
  - Space Complexity: O(1)
  
- Always prefer optimal approaches for better performance (O(n) time complexity and O(1) space complexity).