# Objects

The object initializer syntax starts with an open curly-brace { and ends with a close curly-brace } with a list of </br>
key-value pairs in the middle. Let's take a look at a person object:

```
The object initializer syntax starts with an open curly-brace { and ends with a close curly-brace } with a list of key-value pairs in the middle. Let's take a look at a person object:

const person = {
    hairColor: 'brown',
    toes: 10,
    grumpy: true
}
```

We can retrieve these values by key:

console.log( person.toes ); // 10 </br>
console.log( person.hairColor ); // brown

***Exercise
Let's create an object representing a pizza order! 

In the order object, add the following three keys with values accordingly:

pizzas - Any number greater than zero. </br>
extraCheese - A boolean. Either true or false. </br>
deliveryInstructions - Any string of instructions. </br>

```const order = {
    pizzas: 5,
    extraCheese:  false,
    deliveryInstructions: "officeAddress"
    
};

module.exports = order; ```
