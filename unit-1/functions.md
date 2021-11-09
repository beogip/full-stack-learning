# Functions

Functions are a kind of subroutine that performs a specific task. Like every other programming language, JavaScript has its own rules for declaring functions. Some syntax may seem familiar; however, there are a few things to notice.

## Syntax

The function keyword is placed before the name of the new function to indicate that a new function is being declared. Curly braces {} are used to indicate the function’s body, like most other languages.

```javascript
function HelloWorld(args) {
  // your code
}
```

Keep in mind that Javascript manages reference in arguments dynamically. Primitive values (boolean, number, string) are pass by value. Unlike a primitive value, objects, arrays and functions are pass by reference.

## Code

### Named functions

```javascript
function HelloWorld() {
  console.log("Hello World");
}

HelloWorld(); // will display Hello World
```

### Anonymous functions

In JavaScript, we can make functions without a name called anonymous functions. In the example below, the variable HelloWorld can lose the function declaration and be replaced by any other value.

```javascript
const HelloWorld = function () {
  console.log("Hello World");
};

HelloWorld();
```

### Lambda Functions

Lambda functions are similar to anonymous functions, but they have more flexible features and syntax. An arrow function is another of this type of function. Arrow functions do not bind their own this, instead, they inherit the one from the parent scope, which is called "lexical scoping".

```javascript
const HelloWorld = () => {
  console.log("Hello World"); // Hello World
};

HelloWorld();
```

```javascript
function parentFunction() {
  this.message = "Hello World";
  const HelloWorld = () => {
    console.log(this.message);
  };

  HelloWorld();
}
new parentFunction(); // Hello World
```

## Best practices

- Try to avoid anonymous functions
  - Are created only after declaration. Javascript doesn’t do hoisting like in the case of normal function
  - You can't re use them
  - If you have a large program then debugging is tough because you don’t know the name of the function in the call stack. The call stack will show it as an anonymous function.
  - These functions cannot be unit tested easily. Therefore, you may need to refactor the code.
- A function must do one thing only, and should have a proper name descripting what is doing
- Add early returns every time you can
  - try to check for anomalies at the beginning of the function and terminate the code
  - this technique avoids spaghetti code
