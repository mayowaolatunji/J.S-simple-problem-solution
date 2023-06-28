# LOGICAL OPERATORS

## Logical OR 

There are cases in code where we want to say "this condition" or "this other condition". If either of the conditions are true, let's do something!

It would be quite ugly to write this with if statements every time:

```
if(car) {
    driveToAirport();
}
else if(motorcycle) {
    driveToAirport();
}
else if(truck) {
    driveToAirport();
}
```

If we needed to change the driveToAirport function, we would have to change it in 3 places. It is beneficial to adhere to the principle of code DRYness, which stands for "Don't Repeat Yourself." Whenever feasible, it is advisable to minimize code redundancy and strive for efficient reuse.



Let's try to accomplish the same functionality with the Logical OR (||) operator:

```
if(car || motorcycle || truck) {
    driveToAirport();
}
```

### Task 1

Complete the willEat function. The three arguments will be boolean values (true or false). If any of them are true, return true.

```
function willEat(hasPizza, hasDonuts, hasCookies) {
    
}

module.exports = willEat;
```

---
![Uploading Screenshot 2023-06-23 212346.jpg…]()

## Default Operator

In the last section,  we referred to || as the Logical OR operator.

This operator is also sometimes referred to as the default operator due to its behavior with truthy and falsy values.

Take, for example: `console.log("" || "Something Else"); // Something Else`


`const message = WELCOME_MESSAGE || "Hello there!";` 

 Here the message is guaranteed a truthy value even if WELCOME_MESSAGE is empty.

And it's not just limited to empty strings either:

`const age = user.age || 99;`

 If user.age is undefined or 0 we will default to 99. For that matter user.age could be any falsey value and it would default to 99.

## AND Operator

Another important logical operator is &&, which is called Logical AND:

```
console.log(true && true); // true
console.log(true && false); // false
console.log(false && true); // false
console.log(false && false); // false
```

 Notice that both values must be true for the expression to evaluate to true. We need this to be true AND that to be true as well.

We can, of course, do the same thing with variables:

```
let a = true;
let b = true;

console.log(a && b); // true

b = false;

console.log(a && b); // false
console.log(b && a); // false
```

## Guard Operator

We have learned that the || operator can be called the Logical OR operator or the default operator. Likewise, the && operator can be referred to as the Logical AND operator or the guard operator.

These operators are useful for guarding against run-time exceptions or errors when working with false values.

In the second example, if we tried to retrieve this property directly, we would hit a run-time exception:

```
const user2 = undefined;
console.log(user2.name);
```

Trying to log user2.name right here would result in an uncaught error: Uncaught TypeError: Cannot read property 'name' of undefined.

 Uncaught errors are bad! They'll stop our code execution. This could result in some really ugly errors for users.

```
const friend = { name: "aliu" };

function friendName(friend) {
    return friend && friend.name;
}

module.exports = friendName;
```


## NOT Operator
The final logical operator we will discuss is the "!" operator. Commonly referred to as the NOT or negation operator.

This operator will flip true and false:

```
console.log(!true); // false
console.log(!false); // true
// It will also flip truthy and falsey values:

console.log(!2); // false
console.log(!undefined); // true
```

### ex1: 

In between two towns, there exists a river where a bridge has been constructed to facilitate car crossings. However, the bridge has limited capacity, allowing only one car to pass at a time. This situation poses a problem when both cars attempt to cross simultaneously since neither would be able to pass.

To address this, you are required to implement the carCrossing function, which should return true only when one car is in the process of crossing the bridge.

### solution: 

```
function carCrossing(aCrossing, bCrossing) {
    return ((aCrossing && !bCrossing) || (!aCrossing && bCrossing))
    
    
}

module.exports = carCrossing;
```
