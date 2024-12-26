
# Closures in JavaScript

## Lexical Scope - ??

Closures in JavaScript are a powerful concept that allows functions to retain access to variables from their parent scope even after the parent function has finished executing. This can be achieved by returning a nested function or assigning it to a variable. Closures are commonly used to create private variables and encapsulate data within functions.

## How Closures Work

When a function is defined, it gets a new scope. The magic of closures happens because every function has access to the scope in which it was created. This means that a function can remember and access variables from an outer function scope, even after the outer function has finished executing.

Here's an example:

```javascript
function outerFunction() {
  let outerVariable = "I am outside!";

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

let myInnerFunction = outerFunction();
myInnerFunction(); // logs 'I am outside!'
```

In this example, `innerFunction` is a closure that is returned from `outerFunction`. Even though `outerFunction` has finished executing, `innerFunction` still has access to `outerVariable`.

## Uses of Closures

Closures are commonly used to create data privacy and encapsulation. They can be used to create private variables that can't be accessed from outside the function. They're also used in JavaScript libraries and frameworks for tasks like event handling and callbacks.

```javascript
function createCounter() {
  let count = 0;

  return function () {
    count++;
    return count;
  };
}

let counter = createCounter();
console.log(counter()); // logs 1
console.log(counter()); // logs 2
```

In this example, `count` is a private variable that can't be accessed directly from outside `createCounter`. The inner function returned by `createCounter` forms a closure and has access to `count`.

This is a common use case for closures in JavaScript, where they are used to encapsulate data within a function and create private variables. This pattern is often used in JavaScript to create objects with private state.