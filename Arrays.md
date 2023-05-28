
##Array

When programming, there are often situations where we need to work with multiple elements simultaneously. For example, let's consider a scenario where we have a set of test scores and we want to calculate the average score. In JavaScript, we can use an array to store the scores:

javascript
Copy code
const array = [70, 80, 65, 100, 90, 95];
By using an array, we can easily iterate over its elements and calculate the sum of all the test scores:

let total = 0;
for (let i = 0; i < array.length; i++) {
    total += array[i];
}

Once we have the total sum of all the test scores, we can compute the average by dividing the total by the number of tests in the array:

javascript
Copy code
const average = total / array.length;
Arrays provide us with the capability to store multiple elements, access individual elements using an index, and quickly determine the total number of elements. These features make arrays highly useful in various programming scenarios.

Now, let's further explore the syntax of arrays and practice some exercises to enhance our understanding!
