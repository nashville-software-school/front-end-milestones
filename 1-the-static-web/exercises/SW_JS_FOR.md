# Practicing Iteration

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below, open a terminal window on your **host machine** and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/the-static-web/for-loops && cd $_
touch index.html
touch for-loops.js
```

## Instructions

### Increment by 10

Write a `for` loop that uses a counter variable initialized at 5 and then increments it by 10 every time it executes. Use `console.log()` to output the value of the counter variable each time through the loop. Stop execution of the loop if the counter variable's value is greater than 120.

> **Example output:**
> 
> Current value is 5
>
> Current value is 15
>
> Current value is 25
>
> ...

### Decrement by division

Write a `for` loop with a counter variable initialized at 4096. Each time the loop executes divide the counter variable's value by 2. Use `console.log()` to output its value every time. When the counter variable's value is 1, stop execution.

> **Example output:**
> 
> Current value is 4096
>
> Current value is 2048
>
> Current value is 1024
>
> ...


### Array iteration

Create an array that contains the names of American Presidents. Loop over that array with a `for` loop, and use string concatenation with `console.log()` to output the order and name of each President (see example below).

> **Example output:**
> 
> President #1 was George Washington
>
> President #2 was John Adams
> 
> President #3 was Thomas Jefferson
>
> ...

### Object iteration

Use can use another kind of `for` loop to [iterate over objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in). Iterate over the object below and use `console.log()` to output the names of the keys in the object.

```js
var antSpecies = {
  argentine: {},
  army: {},
  bigHeaded: {},
  black: {},
  bull: {},
  carpenter: {},
  crazy: {},
  fire: {},
  glider: {},
  honeyPot: {},
  jackJumper: {}
}
```

