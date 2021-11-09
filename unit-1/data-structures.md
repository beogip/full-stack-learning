# Basic Data structures

JavaScript has primitive and non-primitive data structures. Primitive data structures and data types are native to the programming language. These include boolean, null, number, string, etc.

Non-primitive data structures are not defined by the programming language but rather by the programmer. These include linear data structures, static data structures, and dynamic data structures, like queue and linked lists.

## Array

The most basic of all data structures, an array stores data in memory for later use. Whenever you’d like to use the array, all you need are the desired indices, and you can access any of the data within.
Arrays in Javascript can change the size in runtime

### Create array

```javascript
let pokemons = ["Bulbasaur", "Squirtle"];

console.log(pokemons.length);
// 2
```

### Access an Array item using the index position

```javascript
let first = pokemons[0];
// Bulbasaur

let last = pokemons[pokemons.length - 1];
// Squirtle
```

## Stack

Are conceptually similar to arrays but stacks process last elements first. This is known as LIFO (last in, first out)

```javascript
const stack = [];
stack.push(2); // stack is now [2]
stack.push(5); // stack is now [2, 5]
const i = stack.pop(); // stack is now [2]
console.log(i); // displays 5
```

## Queues

Are conceptually similar to arrays but queues process elements in the order they enter. This is known as FIFO (first in, first out)

```javascript
const stack = [];
stack.push(2); // stack is now [2]
stack.push(5); // stack is now [2, 5]
const i = stack.shift(); // stack is now [5]
console.log(i); // displays 2
```
