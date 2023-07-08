# Destructuring, Rest & Spread.
![image](https://github.com/mayowaolatunji/J.S-simple-problem-solution/assets/96064869/47134119-2856-4097-acd1-650d1fe16f3f)

## Destructuring

Destructuring is a feature in JavaScript that allows you to extract values from arrays or objects and assign them to variables in a concise way. It provides an elegant syntax to unpack values from complex data structures.

### Array Destructuring:

Array destructuring allows you to extract individual elements from an array and assign them to variables. It follows a pattern similar to the structure of the array. Here's an example:

```
const numbers = [1, 2, 3, 4, 5];
const [a, b, ...rest] = numbers;

console.log(a);      // 1
console.log(b);      // 2
console.log(rest);   // [3, 4, 5]
```

In the above example, the variables a and b capture the first two elements of the numbers array, while the rest operator (...rest) captures the remaining elements into a new array called rest.

### Object Destructuring:

Object destructuring allows you to extract values from an object and assign them to variables. The variable names should match the object property names. Here's an example:

```
const person = {
  name: 'John',
  age: 30,
  city: 'New York'
};

const { name, age, city } = person;

console.log(name);  // 'John'
console.log(age);   // 30
console.log(city);  // 'New York'
```

In the above example, the variables name, age, and city capture the corresponding values from the person object.

## Rest Operator
The rest operator, denoted by ..., allows you to capture multiple elements of an array or object into a new array. It is useful when you want to gather the remaining elements or properties into a separate entity. Here's an example:

```
const numbers = [1, 2, 3, 4, 5];
const [a, b, ...rest] = numbers;

console.log(a);      // 1
console.log(b);      // 2
console.log(rest);   // [3, 4, 5]
```

In the above example, the rest operator collects the remaining elements [3, 4, 5] into the rest array.

## Spread Operator
The spread operator, also denoted by ..., allows you to expand elements of an array or properties of an object into another array or object. It is useful when you want to concatenate arrays or merge objects. Here are a couple of examples:

```
// Array concatenation
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const combinedArray = [...array1, ...array2];

console.log(combinedArray);  // [1, 2, 3, 4, 5, 6]

// Object merging
const obj1 = { x: 1, y: 2 };
const obj2 = { z: 3 };
const mergedObject = { ...obj1, ...obj2 };

console.log(mergedObject);  // { x: 1, y: 2, z: 3 }
```





