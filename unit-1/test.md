# Unit 1 tests

1. Create a function that sums prime numbers. Do it in as few lines as you can.
2. Refactor this function using early return:

```javascript
function FizzBuzz(n) {
  const srt = "";
  if (typeof n === "number") {
    if (n % 3 === 0) {
      if (n % 5 === 0) {
        str = "FizzBuzz";
      } else {
        str = "Fizz";
      }
    } else {
      if (n % 5 === 0) {
        str = "Buzz";
      }
    }
  }
  return str;
}
```

3. Which is the output of the console.log

```javascript
function HiddenMessageGenerator(code) {
  function processCode(code) {
    return (this.code && parseInt(this.code)) || (code && parseInt(code) + 1);
  }

  const processMessage = (code) => {
    if (typeof this.code === "object") {
      return "object detected";
    }
    if (typeof this.code === "string") {
      return "I can't work with a string";
    }
    return `the answer to life the universe and everything is: ${
      this.code * 21
    }`;
  };
  this.code = code;
  this.code = processCode(code);

  this.getMessage = () => processMessage(4);
}

const generator = new HiddenMessageGenerator("1");
console.log(generator.getMessage());
```
