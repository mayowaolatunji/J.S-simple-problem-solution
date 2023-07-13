# Classes & Prototypes

## This Keyword

In JavaScript, the **this** keyword refers to the object that is currently executing or being used within a function or method. Its value is determined by how a function is called or how a method is invoked. The 
**this** keyword allows you to access and manipulate the properties and methods of the current object.

The behavior of **this** can vary depending on the context in which it is used. Here are some common scenarios:

Global scope: If **this** is used outside of any function or object, it refers to the global object, which is usually a window in a web browser or global in Node.js.

Object method: When this is used inside a method of an object, it refers to the object itself. You can use this to access other properties and methods of the object.

```
const obj = {
  name: "John",
  sayHello: function() {
    console.log("Hello, " + this.name + "!");
  }
};


obj.sayHello(); // Output: Hello, John!
```


### Constructor function: 

When a function is used as a constructor (using the new keyword), this refers to the newly created instance of the object. It allows you to assign values to the object's properties.

```
function Person(name) {
  this.name = name;
}

const person = new Person("Alice");
console.log(person.name); // Output: Alice
```

### Event handlers: 

When an event occurs in the browser (e.g., a button click), and the event handler function is executed, this refers to the element that triggered the event.

```
const button = document.querySelector("button");
button.addEventListener("click", function() {
  console.log(this); // Output: the button element
});
```

### Explicit binding: 

You can explicitly bind this to a specific object using methods like call(), apply(), or bind(). These methods allow you to set the value of this within a function, regardless of how it is called.

```
function greet() {
  console.log("Hello, " + this.name + "!");
}

const person = {
  name: "Alice"
};

greet.call(person); // Output: Hello, Alice!
```

It's important to note that the value of this is not determined lexically (based on the code structure), but rather dynamically, depending on how the function is invoked at runtime. Therefore, this can be a common source of confusion, especially when using arrow functions or nested functions, as their behavior differs from regular functions in relation to this.

*** 


## Prototype Chain

#### Prototypes

In many programming languages, classes serve as a blueprint for generating objects known as instances. Every instance possesses its unique collection of properties referred to as state. The class supplies initial state values and functions that are duplicated into each freshly created instance. Classes are templates for creating objects called instances. Each instance will have its own set of properties called state. The class provides initial state values and functions copied into each new instance.

JavaScript does not have classes in a traditional sense. It has prototypes. They function similarily with a few key differences! Primarily, prototypes provide a way to share properties and functions by linking objects together. This is contrary to classes which traditionally copy functionality to new instances.


in JavaScript, every object has an internal property called [[Prototype]] (also referred to as __proto__). This property points to another object, known as the object's prototype. The prototype object itself may have its own prototype, forming a chain of objects linked together, which is called the prototype chain.

The prototype chain is traversed when accessing properties or methods on an object. If a property or method is not found on the object itself, the JavaScript engine follows the prototype chain to find it in the prototype of the object, and if not found there, it continues up the chain until it reaches the end of the chain, which is typically Object.prototype.

Let's consider an example to illustrate the prototype chain:


```
// Constructor function
function Person(name) {
    this.name = name;
}

// Creating objects using the constructor
const person = new Person("John");

console.log(person.name); // "John"
```

In this example, we have a constructor function Person that sets the name property on the newly created objects. When we create an object person using the new keyword, the [[Prototype]] of person is set to Person.prototype. So, Person.prototype acts as the prototype for person.

The Person.prototype object is a regular JavaScript object. It can have properties and methods that will be shared among all instances created using the Person constructor function. For example:


```
Person.prototype.sayHello = function() {
    console.log("Hello, my name is " + this.name);
};

person.sayHello(); // "Hello, my name is John"
```

Here, the sayHello method is added to Person.prototype. Now, person can access and invoke this method even though it is not defined directly on person itself. This is possible due to the prototype chain. When we call person.sayHello(), JavaScript first looks for the sayHello method on person. Since it is not found, it follows the prototype chain to Person.prototype and finds the method there.

The prototype chain allows for efficient reuse of code and memory. Rather than creating a separate copy of each method for every instance, methods are shared among objects through their prototype chain. This means that changes made to the prototype object will be reflected in all instances that inherit from it.

It's important to note that the prototype chain is not limited to a single level. Objects can have their own prototypes, which in turn can have their prototypes, forming a chain of objects. When accessing a property or method, JavaScript will traverse the prototype chain until it finds the property or reaches the end of the chain (Object.prototype). This enables multiple levels of inheritance and allows for complex object relationships.
