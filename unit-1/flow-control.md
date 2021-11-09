# Flow control

Exists several structures to conditionally run code in runtime.

- [if](#if)
- [if-else](#if-else)
- [if-else-if](#if-else-if)
- [ternary](#Ternary)
- [switch](#switch)
- [for](#for)

### if

if statement is the most simple decision making statement. It is used to decide whether a certain statement or block of statements will be executed or not.

```
if (condition) {
   // Statements to execute if
   // condition is true
}
```

Another way to declare if statements:

```
if (condition)
  statement1
statement2
```

Statement1 will run only if the condition is true, statement2 will always run. Keep in mind that this way to declare is only afecting the next line after the if.

### if-else

Similar to the if, in this statement we have one **if** block followed with an **else**. This new part will run if the condition is false

```
if(condition){
  // Statements to execute if
  // condition is true
}else{
  // Statements to execute if
  // condition is false
}
```

### if-else-if

With this statement you can add a contitional to the else block

```
if(condition){
  // Statements to execute if
  // condition is true
}else if(condition2){
  // Statements to execute if
  // condition2 is true
}else{
  // Statements to execute if
  // condition is false and condition2 is false
}
```

### Ternary

This operator allows you to assign a value to a variable using conditionals.

```
// if contition is true foo will have the value1,
// otherwiser the value will be value2
let foo = condition ? value1 : value2;
```

Another way to conditionally assign a value to a variable is using the operator || (or)

```
//if value1 is not a falsy value (undefined, null, 0, '', NaN)
//foo will have the value of value1
//Otherwise, it will have value2 as value
let foo = value1 || value2
```

### Switch

The switch case statement in JavaScript is also used for decision making purposes. In some cases, using the switch case statement is seen to be more convenient over if-else statements. The switch case will evaluate the expression and run the block inside the correspond case. Keep in mind if you don't add the break statement and the condition matches it will run the next block.

```
switch (expression)
{
    case value1:
        statement1;
        break;
    case value2:
        statement2;
        break;
    ...
    case valueN:
        // if expression matches with this case, since it
        // doesn't have a break, the block "default" will run
        statementN;
    default:
        // this block will run if expresssion doesn't match with
        // any case
        statementDefault;
}
```

### for

The following for statement starts by declaring the variable i and initializing it to 0. It checks that i is less than nine, performs the two succeeding statements, and increments i by 1 after each pass through the loop.

```javascript
for (let i = 0; i < 9; i++) {
  console.log(i);
  // more statements
}
```

### for-in

The for...in statement iterates over all enumerable properties of an object that are keyed by strings, including inherited enumerable properties.

```javascript
const object = { a: 1, b: 2, c: 3 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```

### for-of

The for...of statement creates a loop iterating over iterable objects, including: built-in String, Array, array-like objects.

```javascript
const array1 = ["a", "b", "c"];

for (const element of array1) {
  console.log(element);
}

// expected output: "a"
// expected output: "b"
// expected output: "c"
```
