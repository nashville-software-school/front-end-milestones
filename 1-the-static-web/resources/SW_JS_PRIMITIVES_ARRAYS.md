# Javascript: Primitives & Arrays

> There is a popular paradox stated about JavaScript. "Because JavaScript can be used without understanding, the understanding of the language is often never attained."

You will not be one of those people. You will understand the power, complexities, and versatility of JavaScript when you leave this cohort.

## Overview

Javascript is **the most important language** you will use as a front end developer, and possibly for much of your career, because it is the language of the web browser. All browser based applications - Facebook, Twitter, Etsy, Pinterest - are all written with JavaScript.

## The Alert

Use alert to show messages to people using your application.

`alert("Thank you for using our product");`

## Variables

Learn how to store values in human readable variables that can be used throughout your code, and changed when necessary. It is the same as your bank account number. That number never changes, but the actual value of your bank account changes daily as you make money and spend money.

### Number values

You bank account number is a variable, and the money contained in it is the value of the variable. In JavaScript, you can create a variable name that will hold any value you want.

`var bankAccount = 1000;`

Now, anywhere else in the code that you use the `bankAccount` variable, the value of 1000 will actually be used.

`var combinedAccount = 2000 + bankAccount;`

The new variable called `combinedAccount` will now hold the value 3000.

### String values
Variables can hold all kinds of values. Here's one holding a string value. Strings are a continuous collection of letters and values inside two quote characters.

```
var instructor = "Steve";
var numberOfStudents = "15";
```

### Boolean values

These variables will hold the value of `true` or `false`.

```
var studentsAreAwesome = true;
var limaBeansAreYummy = false;
```

### Declaring variables

You can declare a variable first, and then assign it a value later.
```
var fruit;
fruit = "apple";
```

But, as we saw before, you can declare it and assign it a value on the same line of code.
```
var fruit = "apple";
```

### Changing variable values

Declare a variable and give it an initial value.

```
var name = "Beth";
```

You can modify the value of a variable at any time, which is why they are called variables, because their value varies any time you want.

```
var name = "Susan";
```

If you tried to use the variable `name` at this point, it's value would be `Susan` even though you initially provided the value of `Beth`.

## Math Expressions

How to do math with JavaScript. Show the main mathematical operators, and their use with integer value variables.

`+`,`-`,`/`,`%`, `*`

## The console

Learn how to output the value of variables to the browser's console.

```
console.log("Hello, world!");
```

## Arrays

Arrays are like buckets that you can use to store a collection numbers and/or strings.

```
var commands = ["blue", 42, "shift left", "hut"];
```

### Adding/removing items to an array

You can specify a value to place at a specific index (position).

```
commands[0] = "periwinkle";
commands[3] = 24;

// ["periwinkle", 42, "shift left", 24]
```

You can use the `push()` method which is available on an variable that holds an array. This method puts a new item on the end of the array.

```
commands.push("hot route");

// ["periwinkle", 42, "shift left", 24, "hot route"]
```

To remove the last item, you have to `pop()` it off.

```
var lastOne = commands.pop();

// ["periwinkle", 42, "shift left", 24]
// lastOne now contains the value "hot route"
```

The `unshift()` and `shift()` methods add and remove items from the beginning of the array.

1. When trying to find out what's causing an error in your code, a useful command is the [debugger](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/debugger) statement. Try putting it in your code and watch what happens when you run it in Chrome.
1. Now that you know how to declare variables, you can learn about how JavaScript [hoists](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var#var_hoisting) variable declarations.
1. Learn how to assign the [same value to two variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var#Assigning_two_variables_with_single_string_value) with a single line of code.