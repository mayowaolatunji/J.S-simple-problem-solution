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
