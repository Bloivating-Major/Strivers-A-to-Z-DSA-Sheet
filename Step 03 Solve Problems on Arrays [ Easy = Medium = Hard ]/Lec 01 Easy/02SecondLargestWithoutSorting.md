# Lecture 01: Find the Second Largest and Second Smallest Element in an Array 🥈🔢

Finding the second largest and second smallest elements in an array is a common interview question. There are several approaches, ranging from brute force to optimal solutions.

## Brute Force Approach 🐢

- Sort the array in ascending order.
- The largest element is at the last index.
- Traverse backwards to find the first element smaller than the largest (second largest).

```javascript
let arr = [2, 3, 5, 9, 9, 6, 9, 4];

arr.sort((a,b) => a-b);

let n = arr.length;
let largest = arr[n-1];
let secondLargest = -1;

for(let i = n-2; i >= 0; i--){
    if(arr[i] !== largest) {
        secondLargest = arr[i];
        break;
    } 
}

console.log('Largest:', largest);         // Output: 9
console.log('Second Largest:', secondLargest); // Output: 6
```

## Better Solution ⚡

- Find the largest element in one pass.
- In another pass, find the largest element that is not equal to the largest (second largest).

```javascript
let largest = arr[0];
let n = arr.length;

for(let i = 1; i < n; i++){
    if(arr[i] > largest) largest = arr[i];
}

let secondLargest = -1;

for(let i = 0; i < n; i++){
    if(arr[i] > secondLargest && arr[i] !== largest) secondLargest = arr[i];
}

console.log('Largest:', largest);
console.log('Second Largest:', secondLargest);
```

## Summary 🎉

- Brute force uses sorting and extra passes.
  - Time Complexity: O(n log n)
  - Space Complexity: O(1)
- Better solution uses two passes.
  - Time Complexity: O(n)
  - Space Complexity: O(1)