Variables declared with var are in the function scope. var is hoisted.

Variables declared with let are in the block scope.

Variables declared with const are in the block scope. It does not define a constant value. It defines a constant reference to a value.

Are let, const hoisted??

# JavaScript Variables

JavaScript has three different ways to declare a variable, each with its own scope and hoisting behavior.

## var

Variables declared with `var` are function-scoped. This means they are only accessible within the function they are declared in. `var` variables are hoisted, which means they are moved to the top of their containing scope. However, when hoisted, they are initialized with `undefined`.

```javascript
console.log(myVar);
var myVar = 'var';
```

## let
Variables declared with `let` are block-scoped. This means they are only accessible within the block they are declared in. `let` variables are also hoisted, but they are not initialized. If you try to access a `let` variable before it's declared, you'll get a ReferenceError.

```javascript
console.log(myLet);
let myLet = 'let';
```

## const

Variables declared with `const` are block-scoped, like `let`. The const keyword does not define a constant value, but a constant reference to a value. This means that the variable cannot be reassigned, but if it's an object or array, its properties or elements can be modified. `const` variables are hoisted in the same way as `let` variables.

```javascript
console.log(myConst);
const myConst = 'const';
```