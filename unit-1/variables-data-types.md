# Variables and data-types

## Data-types

Javascript is a Dynamically typed language: it's means that a variable can receive different data types over run time.

```javascript
var str = 'some string' // first value of str is an string
...
str = 5 // now str stores a number
```

The latest version of JavaScript(ES6) defines seven data types:

- **Numbers:** 5, 6.5, 7 etc.
- **String:** “Hello world" etc.
- **Boolean:** Represent a logical entity and can have two values: true or false.
- **Null:** This type has only one value : null.
- **Undefined:** A variable that has not been assigned a value is undefined.
- **Object:** It is the most important data-type and forms the building blocks for modern JavaScript.

## Variables

Variables in JavaScript are containers that hold reusable data. It is the basic unit of storage in a program.

The value stored in a variable can be changed during program execution.
A variable is only a name given to a memory location, all the operations done on the variable effects that memory location.
In JavaScript, all the variables must be declared before they can be used.

ES6 have three different variable containers: **var**, **let** and **const**.

Var was the first way to declare variables. This kind of variables are function scoped and can be modified after declared

```javascript
// declaring single variable
var name;

// declaring multiple variables
var name, title, num;

// initializing variables
var name = "Foo";
name = "Bar"; // name's end value is "Bar"

var name = "Foo";
function someFunction() {
  // this variable only exists inside the function someFunction
  var name = "Bar";
}
console.log(name); // "Foo"
```

Let is similar to var but unlike var is block scoped

```javascript
// declaring single variable
let name;

// declaring multiple variables
let name, title, num;

// initializing variables
let name = "Foo";
name = "Bar"; // name's end value is "Bar"

let name = "Foo";
function someFunction() {
  // this variable only exists inside the function someFunction
  let name = "Bar";
  if (name == "Bar") {
    let title = "Some Title";
  }
  console.log(title); // Error title is not defined
}
console.log(name); // "Foo"
```

To declare constants in Javascript you need to use the container const

```javascript
// Constant
const name = "Foo";
name = "Bar"; // will give Assignment to constant variable error.
```

## Variable scope

Javascript has two different scopes:

- **Global:** scope outside the outermost function attached to Window.
- **Local:** Inside the function being executed.

```javascript
let globalVar = "This is a global variable";

function fun() {
  let localVar = "This is a local variable";

  console.log(globalVar); // This is a global variable
  console.log(localVar); // This is a local variable
}
fun();

console.log(globalVar); // This is a global variable
console.log(localVar); // Error localVar is not defined
```
