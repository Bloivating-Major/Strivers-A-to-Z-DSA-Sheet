# Lecture 06: Find the Highest & Lowest Frequency of Elements in JavaScript 📈📉

Finding the highest and lowest frequency of elements in an array is a common task in data analysis and coding interviews. Hashing makes it efficient!

## Why Find Frequencies? 🤔

- Identify the most or least common elements
- Solve problems like "majority element" or "least frequent element"
- Analyze patterns in data

## Approach: Use a Hash Map to Count Frequencies 🚀

1. Count the frequency of each element using an object or Map.
2. Iterate through the frequency map to find the highest and lowest counts.

## Example Code 💻

```javascript
function findHighLowFrequency(arr) {
  let freq = {};
  for (let num of arr) {
    freq[num] = (freq[num] || 0) + 1;
  }

  let highest = -Infinity, lowest = Infinity;
  let highElem, lowElem;

  for (let key in freq) {
    if (freq[key] > highest) {
      highest = freq[key];
      highElem = key;
    }
    if (freq[key] < lowest) {
      lowest = freq[key];
      lowElem = key;
    }
  }

  return {
    highestFrequency: { element: highElem, count: highest },
    lowestFrequency: { element: lowElem, count: lowest }
  };
}

let numbers = [1, 2, 2, 3, 1, 4, 2, 4, 4];
console.log(findHighLowFrequency(numbers));
// Output: { highestFrequency: { element: '2', count: 3 }, lowestFrequency: { element: '3', count: 1 } }
```

## Summary 🎉

- Use hashing to count frequencies efficiently.
- Scan the frequency map to find the highest and lowest frequency elements.
- This technique is useful for many coding and data analysis problems!