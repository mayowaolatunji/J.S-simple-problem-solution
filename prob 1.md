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

# 4

Count Vowels
Write a function countVowels that takes in a string and counts how many vowels there are in the word. Vowels include: "a", "e", "i", "o", and "u".

Handle lowercase and uppercase vowels.

## Solution 

```
function countVowels(str) {
    let j = 0;
    for (let i = 0; i < str.length; i++) {
        const char = str[i].toLowerCase();
        if (char === "a" || char === "e" || char === "i" || char === "o" || char === "u") {
            j++;
        }
    }
    return j;
}
```

module.exports = countVowels;

**NOTE: **

- We introduce a new variable char that stores the lowercase version of the character at each index i in the string. This is achieved using the toLowerCase() method.

- We modify the if condition to compare char (lowercase) with the lowercase vowels ("a", "e", "i", "o", "u"). By converting both char and the comparison vowels to lowercase, we can perform a case-insensitive comparison.


# 5

Reverse: 
Write a function reverse that takes a string as an argument and returns a string with all the letters reversed.

For example, reverse("cat") would return the string "tac".

## Solution

```
function reverse(string) {
    let j = "";
    for (let i = string.length - 1; i >= 0; i--) {
        j += string[i];
    }
    return j;
}

module.exports = reverse;

```
# 6

Palindrome: 
Write a function isPalindrome that takes a word string and returns true if the word is a palindrome or false if it is not.

A palindrome is a word that is spelled the same forwards as it is backwards.

 The word pop is a palindrome.

## Solution

```
function isPalindrome(string) {
    let j = "";
    for (let i = 0; i<=string.length; i++){
        if (string[i] === string[string.length -1-i]){
            return true

        } else {
            return false

        }
        
    }

}

module.exports = isPalindrome;
```
