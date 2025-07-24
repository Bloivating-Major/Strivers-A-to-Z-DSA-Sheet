# Lecture 06: Counting Frequency of Array Elements in JavaScript 🔢📊

Counting how often each element appears in an array is a common task in programming. Hashing makes this process efficient and easy!

## Why Count Frequency? 🤔

- Find duplicates or unique elements
- Analyze data patterns
- Solve problems like "most frequent element" or "majority element"

---

## Approach 1: Using a Hash Map (Object or Map) 🚀

- Loop through the array
- For each element, increment its count in a hash map

### Example with Object

```javascript
function countFrequency(arr) {
  let freq = {};
  for (let num of arr) {
    freq[num] = (freq[num] || 0) + 1;
  }
  return freq;
}

let numbers = [1, 2, 2, 3, 1, 4, 2];
console.log(countFrequency(numbers));
// Output: { '1': 2, '2': 3, '3': 1, '4': 1 }
```

### Example with Map 🗺️

```javascript
function countFrequency(arr) {
  let freq = new Map();
  for (let num of arr) {
    freq.set(num, (freq.get(num) || 0) + 1);
  }
  return freq;
}

let numbers = [5, 6, 5, 7, 6, 5];
console.log(countFrequency(numbers));
// Output: Map { 5 => 3, 6 => 2, 7 => 1 }
```

---

## Approach 2: Brute Force (Nested Loops) 🐢

This method uses a nested loop and a visited array to avoid counting the same element multiple times.  
**Time Complexity:** O(n²)

```javascript
let arr = [10, 5, 10, 15, 10, 5, 5, 5];
let n = arr.length;

function freqCount(arr, n){
    let visited = new Array(n).fill(false);
    for(let i = 0; i < n; i++){
        let count = 1;
        if(visited[i] === true) continue;
        for(let j = i + 1; j < n; j++){
            if(arr[i] === arr[j]){
                count++;
                visited[j] = true;
            }
        }
        console.log(arr[i] + ' ' + count);
    }
}

freqCount(arr, n);
// Output:
// 10 3
// 5 4
// 15 1
```

---

## Approach 3: Using Map for Efficient Counting ⚡

This method uses a Map for O(n) time complexity.

```javascript
let arr = [10, 15, 5, 10, 15, 10];
let n = arr.length;

function countFreq(arr, n){
    let map = new Map();
    for(let i = 0; i < n; i++){
        map.set(arr[i], (map.get(arr[i]) || 0) + 1);
    }
    console.log(map);
}

countFreq(arr, n);
// Output: Map { 10 => 3, 15 => 2, 5 => 1 }
```

---

## Summary 🎉

- Hashing lets you count frequencies in O(n) time.
- Use objects or Map for efficient frequency counting.
- Brute force works but is slower for large arrays.
- This technique is useful for many coding and data analysis problems!