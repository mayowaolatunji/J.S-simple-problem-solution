# Destructuring, Rest & Spread.
![image](https://github.com/mayowaolatunji/J.S-simple-problem-solution/assets/96064869/47134119-2856-4097-acd1-650d1fe16f3f)

The code you provided defines a function named throwError. This function creates an empty array a and then checks if the length of a is less than 5. If the length is less than 5, it throws an Error object with the message "we dont want a to be < 5".

It seems there is a small mistake in the code. The correct way to check the length of an array is by using the length property directly on the array object (a.length), rather than using length(a).

*Here's the corrected code:*

```
function throwError() {
    let a = [];
    if (a.length < 5) {
        throw new Error("we don't want a to be < 5");
    }
}

module.exports = throwError;
```
