
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



## Case Study 

Code 1:


`function hasOne(array) {

    for (i =0; i<= array.length; i++) {
    
        if (array[i] === 1) {
        
            return true;
            
        } else {
            return false;
            
        }
    }
}

module.exports = hasOne;`

In Code 1, the loop condition is i <= array.length, which includes the length of the array. The loop iterates over the array elements, and in the first iteration itself, it checks if the element at index 0 is equal to 1. If it is, it immediately returns true. If it's not, it returns false. In either case, the function terminates after the first iteration.

Code 2:


`function hasOne(array) {

    for (let i =0; i< array.length; i++) {
    
        if (array[i] === 1) {
            return true;
            
        }
    }
    return false;
}

module.exports = hasOne;`
In Code 2, the loop condition is i < array.length, which excludes the length of the array. The loop iterates over the array elements, and if it finds an element equal to 1, it immediately returns true. If the loop completes without finding any 1 in the array, it reaches the return false statement outside the loop and returns false.

The key difference is that Code 1 returns a result after the first iteration, while Code 2 iterates over the entire array and returns false only if no 1 is found. Code 2 allows for multiple iterations and a proper examination of all elements in the array before reaching a final result.


## Running Value

We can keep a running value while we're looping over an array. There are many reasons we might do this. For instance, if we wanted to find the average of many numbers like:

`const result = average([80,90,98,100]); 

console.log( result ); // 92`

The average function will want to loop over the array and keep a running total of the values. Then it will divide by the length of the array to find the average:

`function average(array) {

    let total = 0;
    
    for(let i = 0; i < array.length; i++) {
        total += array[i];
        
    }
    return (total / array.length);
}`


### problem 1 (running value)

Find the Sum of Even Values
Given an array, find the sum of all even values inside the array and return it.

**Solution**
Initialize a variable total to 0. This variable will store the running sum of even values.

Use a for loop to iterate over each element of the array. The loop starts from index 0 and goes up to array.length, inclusive.

Inside the loop, check if the element at index i is even by using the modulus operator %. If the remainder of dividing the element by 2 is 0, it means the element is even.

If the element is even, add it to the total using the += operator. This accumulates the sum of all even values encountered so far.

After iterating over all elements, the loop terminates, and the function returns the final value of total, which represents the sum of all even values in the array.

`function sumEven(array) {
total = 0;
    for (let i =0; i <= array.length; i++){
        if (array[i] %2 === 0){
        
            total += array[i]
                }
    }
    return total
}

module.exports = sumEven;`

