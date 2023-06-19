# 1

 Your Goal: Find the Shorter String
The function shortestString takes two string arguments: str1 and str2.

Determine which of the two strings is shorter, return that string.

## Solution 

```
function shortestString(str1, str2) {
    if (str1.length < str2.length) {
        return str1;
    } else {
        return str2;
    }
}

module.exports = shortestString;
```

# 2

The function halfValue takes an array of numbers. It should return a new array with all the original values halved.

Odd numbers should be rounded up to the nearest whole number.

## Solution 

```
function halfValue(numbers) {
    let n = [];
    for (let i = 0; i < numbers.length; i++) {
        n.push(Math.round(numbers[i] / 2));
    }
    return n;
}

module.exports = halfValue;

```
