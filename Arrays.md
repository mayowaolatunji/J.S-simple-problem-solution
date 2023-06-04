
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


` function hasOne(array) {`

    for (i =0; i<= array.length; i++) {
    
        if (array[i] === 1) {
        
            return true;
            
        } else {
            return false;
            
        }
    }
}
`module.exports = hasOne; `

In Code 1, the loop condition is i <= array.length, which includes the length of the array. The loop iterates over the array elements, and in the first iteration itself, it checks if the element at index 0 is equal to 1. If it is, it immediately returns true. If it's not, it returns false. In either case, the function terminates after the first iteration.

Code 2:


`function hasOne(array) {`
    for (let i =0; i< array.length; i++) {
    
        if (array[i] === 1) {
            return true;
            
        }
    }
    return false;
}

`module.exports = hasOne;`

In Code 2, the loop condition is i < array.length, which excludes the length of the array. The loop iterates over the array elements, and if it finds an element equal to 1, it immediately returns true. If the loop completes without finding any 1 in the array, it reaches the return false statement outside the loop and returns false.

The key difference is that Code 1 returns a result after the first iteration, while Code 2 iterates over the entire array and returns false only if no 1 is found. Code 2 allows for multiple iterations and a proper examination of all elements in the array before reaching a final result.


## Running Value

We can keep a running value while we're looping over an array. There are many reasons we might do this. For instance, if we wanted to find the average of many numbers like:

`const result = average([80,90,98,100]); 

console.log( result ); // 92`

The average function will want to loop over the array and keep a running total of the values. Then it will divide by the length of the array to find the average:

`function average(array) {`

    let total = 0;
    
    for(let i = 0; i < array.length; i++) {
        total += array[i];
        
    }
    return (total / array.length);
`}`


### problem 1 (running value)

Find the Sum of Even Values
Given an array, find the sum of all even values inside the array and return it.

**Solution**
Initialize a variable total to 0. This variable will store the running sum of even values.

Use a for loop to iterate over each element of the array. The loop starts from index 0 and goes up to array.length, inclusive.

Inside the loop, check if the element at index i is even by using the modulus operator %. If the remainder of dividing the element by 2 is 0, it means the element is even.

If the element is even, add it to the total using the += operator. This accumulates the sum of all even values encountered so far.

After iterating over all elements, the loop terminates, and the function returns the final value of total, which represents the sum of all even values in the array.

`function sumEven(array) {`

total = 0;
    for (let i =0; i <= array.length; i++){
        if (array[i] %2 === 0){
        
            total += array[i]
                }
    }
    return total
}
`module.exports = sumEven;`


## Returning New arrays

When we need to filter an array based on certain conditions, we can create a new array and add the elements to it if they meet our criteria.

For example, if we want to filter an array to include only numbers that are greater than 10:

` function greaterThanFive(array) {`

    const newArray = [];
    for(let i = 0; i < array.length; i++) {
        const element = array[i];
        
        // is this element greater than 10?
        if(element > 10) {
        
            // yes, push this element on our array
            newArray.push(element);
        }
    }
   ` return newArray;}`
   
In this scenario, the approach involves creating a new array (newArray) and selectively adding elements from the original array to it based on a specific condition. In this case, the condition is that the element should be greater than 10. Finally, the new array is returned as the result.

By iterating over each element in the original array, the code checks if the element is greater than 10. If the condition is satisfied, the element is added to the newArray using the push method. Finally, the newArray is returned as the result, containing only the elements that are greater than 10 from the original array.


## To Write a function that will take an array of numbers and return a new array that only contains unique numbers.

```
function unique(array) {
   
   const newArray = [];
   for (let i = 0; i < array.length; i++) {
        const digit = array[i];

        if (newArray.indexOf(digit) === -1) {
            newArray.push(digit);
        }
    }

    return newArray;
}
module.exports = unique;
```


- The unique function takes an input array and returns a new array containing only the unique elements from the input array. Here's a detailed explanation of the code:

- const newArray = [];: This line initializes an empty array newArray that will store the unique elements.

- for (let i = 0; i < array.length; i++) {: This is a for loop that iterates over each element in the input array.

- const element = array[i];: Inside the loop, the current element of the array is assigned to the variable element. This allows easier reference to the element during comparison and manipulation.

- if (newArray.indexOf(element) === -1) {: This condition checks if the element is not already present in the newArray. The indexOf method is used to search for the element in newArray. If the element is not found (returns -1), it means it is unique.

- newArray.push(element);: If the element is unique, it is added to the newArray using the push method. This ensures that only unique elements are included in the newArray.

- After the loop finishes iterating over all elements in the input array, the newArray is returned as the result.
