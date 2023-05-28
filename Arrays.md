
# Array

When programming, there are often situations where we need to work with multiple elements simultaneously. For example, let's consider a scenario where we have a set of test scores and we want to calculate the average score. In JavaScript, we can use an array to store the scores:


```const array = [70, 80, 65, 100, 90, 95];```

By using an array, we can easily iterate over its elements and calculate the sum of all the test scores:


let total = 0;
for (let i = 0; i < array.length; i++) {
    total += array[i];}

Once we have the total sum of all the test scores, we can compute the average by dividing the total by the number of tests in the array:

const average = total / array.length;

Arrays provide us with the capability to store multiple elements, access individual elements using an index, and quickly determine the total number of elements. These features make arrays highly useful in various programming scenarios.

**If we need to store a collection of elements in Javascript, we utilize an Array.

An array is denoted by an opening square bracket [ at the beginning and a closing square bracket ] at the end. The elements contained within the array are separated by commas ,.

Here are a few examples of arrays containing primitive data types:

```const numbers = [1, 2, 3, 4, 5];```

```const booleans = [true, false, true, true];```

```const strings = ["happy", "go", "lucky"];```

Furthermore, it is also possible to store arrays inside other arrays, creating a structure known as a nested array.

```const nested = [[1, 2, [1, 2]], 2];```
