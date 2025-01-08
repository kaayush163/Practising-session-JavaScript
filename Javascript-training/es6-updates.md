# ES6 Updates

ES6, also known as ECMAScript 2015, introduced several significant updates to JavaScript. Here are some of the key features:

## `let` and `const`

`let` and `const` provide block-level scoping, which is a more intuitive and safer way to declare variables. `let` is for variables that will change, and `const` is for variables that won't change.

## Arrow Functions

Arrow functions provide a new syntax for writing functions in JavaScript. They are particularly useful for short, single-line functions.

```javascript
const square = x => x * x;
```

Arrow functions are not hoisted. They must be defined before they are used. Arrow functions do not have their own `this`.

## Template Literals

Template literals allow for easier string interpolation, multi-line strings, and can embed expressions. They are enclosed by the backtick (` `) character instead of double or single quotes.

```javascript
let name = 'John';
console.log(`Hello, ${name}!`);  // Outputs: Hello, John!
```

### Destructuring Assignment

Destructuring assignment syntax makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

```javascript
let [a, b] = [1, 2];
let {name, age} = {name: 'John', age: 30};
```

### Default Parameters

Default function parameters allow named parameters to be initialized with default values if no value or undefined is passed.

```javascript
function greet(name = 'World') {
  console.log(`Hello, ${name}!`);
}
```

### Promises

Promises in JavaScript represent a completion or failure of an asynchronous operation and its resulting value. A `Promise` is in one of these states:

- `pending`: initial state, neither fulfilled nor rejected.
- `fulfilled`: meaning that the operation completed successfully.
- `rejected`: meaning that the operation failed.

A promise is said to be settled if it’s either fulfilled or rejected.

Here's a simple example of a Promise:

```javascript
let promise = new Promise(function(resolve, reject) {
  // After a delay of one second, the promise will be resolved with the value "Done!"
  setTimeout(() => resolve("Done!"), 1000);
});

promise.then(
  result => console.log(result), // Outputs: "Done!"
  error => console.log(error) // Not called
);
```

### Modules

ES6 introduced a module system to JavaScript, allowing you to import and export functions, objects, or values from module to module.

### Classes

ES6 introduced a class keyword for defining classes in JavaScript, providing a much cleaner and object-oriented class syntax.

### Spread and Rest Operators

The spread operator allows an iterable to expand in places where zero or more arguments or elements are expected. The rest parameter syntax allows us to represent an indefinite number of arguments as an array.

### Enhanced Object Literals

ES6 enhanced object literals to include shorthand syntax for initializing properties from variables and defining function methods, support for computed names in object property definitions, and methods for including prototypes during object creation.