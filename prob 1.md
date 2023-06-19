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

# 3

Your Goal: Count the C's
The function countC takes a string str as its only argument.

This function should return the number of c's found in the string. It must count both lower-case c and upper-case C.

## Solution 

```
function countC(str) {
    let j = 0;
    for (let i = 0; i < str.length; i++) {
        if (str[i] === "c" || str[i] === "C") {
            j++;
        }
    }
    return j;
}

module.exports = countC;

```
