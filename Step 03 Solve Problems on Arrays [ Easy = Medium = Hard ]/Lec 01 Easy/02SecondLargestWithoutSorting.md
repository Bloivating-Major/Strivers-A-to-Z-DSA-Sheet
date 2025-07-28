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

## Optimal Solution 🏅

- Find both the largest and second largest in a single pass.
- Similarly, find the smallest and second smallest in a single pass.

```javascript
function sLargest(arr){
    let n = arr.length;
    let largest = arr[0];
    let sLargest = -1;
    for(let i = 1; i < n; i++){
        if(arr[i] > largest){
            sLargest = largest;
            largest = arr[i];
        }
        else if(arr[i] > sLargest && arr[i] < largest){
            sLargest = arr[i];
        }
    }
    console.log('Largest is ', largest);
    console.log('Second Largest is ', sLargest);
}

function sSmallest(arr){
    let n = arr.length;
    let smallest = arr[0];
    let sSmallest = Infinity;
    for(let i = 1; i < n; i++){
        if(arr[i] < smallest){
            sSmallest = smallest;
            smallest = arr[i];
        }
        else if(arr[i] < sSmallest && arr[i] > smallest){
            sSmallest = arr[i];
        }
    }
    console.log('Smallest is ', smallest);
    console.log('Second Smallest is ', sSmallest);
}

sLargest(arr);
sSmallest(arr);
```

## Summary 🎉

- Brute force uses sorting and extra passes.
  - Time Complexity: O(n log n)
  - Space Complexity: O(1)
- Better solution uses two passes.
  - Time Complexity: O(n)
  - Space Complexity: O(1)
- Optimal solution finds second largest and smallest in a single pass.
  - Time Complexity: O(n)
  - Space Complexity: O(1)
- Always prefer optimal approaches for better performance (O(n) time complexity).