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

### We can retrieve these values by key:

console.log( person.toes ); // 10 </br>
console.log( person.hairColor ); // brown

We can use the . property accessor operator or we can use brackets [] just like with arrays! </br>
console.log( team.name ); // Mets
console.log( team['name'] ); // Mets


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

module.exports = order; 
```


## Array of Objects

Things get really interesting when we start to put objects inside arrays and vice-versa!

Let's take our team example again:

```const team = {
    name: "Mets",
    wins: 86,
    inPlayoffs: false,
};
```

In a league, we might have many teams:

```const teams = [team1, team2, team3];
for(let i = 0; i < teams.length; i++) {
    console.log(teams[i].name); 
}
```


## Typed Orders

Code is more readable and mantainable when numbers are defined.

Take the following example:

```
const card = {
    suit: 1,
    value: 5
}
```

What is this card's suit? We know the value is 1, but what does that mean? 

Let's define CARD_SUITS:

```
const CARD_SUITS = {
    DIAMONDS: 0,
    HEARTS: 1,
    SPADES: 2,
    CLUBS: 3
}
```
Using this object we can clearly label our card suit:

```
const card = {
    suit: CARD_SUITS.HEARTS,
    value: 5
}
```


### Task

Modify the numberOfPizzas function to only count pizzas when the order.type is equal to ORDER_TYPES.PIZZA.

The orders will have a type keyword:

```
const orders = [
    { pizzas: 3, type: ORDER_TYPES.PIZZA },
    { wings: 12, type: ORDER_TYPES.WINGS },
];
```

