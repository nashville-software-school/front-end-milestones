# Javascript: If/else, Switch & For

## Conditions with *if* and *else*

Check if something is true or false and then execute different code for each case.

> **Tip: ** There are several types of punctuation in JavaScript. {} are braces, [] are brackets, () are parenthesis, <> are angle brackets.

```
if (studentsAreAwesome) {
   alert("Congratulations!! You get a new career.");
}
```

If `studentsAreAwesome` was **false**, then the alert would not be shown. Use the else condition to handle when your evaluation is false.

```
if (studentsAreAwesome) {
   alert("Congratulations!! You get a new career.");
} else {
   alert("Back to the plutonium mines for you!");
}
```

## Switch statement

```js
var value = 10;
switch (value) {
  case 1:
    console.log("Small number");
    break;
  case 5:
    console.log("Medium number");
    break;
  case 10:
    console.log("Large number");
    break;
  default:
    console.log("Dunno");
}
```

## Loops with *for*

The *for* loop allows you to execute the same logic over and over again, a predetermined number of times.

First, you state an initial value that will be checked the first time through the loop.

```
for (var count = 1;;) {
   // Do something
}
```
Next, you put in a condition check. If it evaluates to true, then the logic inside the loop will execute.
```
for (var count = 1; count < 10;) {
   // Do something
}
```
The last element is what will be executed each time through your loop. In this example, we're simply going to increase the value of our `count` variable by 1.
```
for (var count = 1; count < 10; count = count + 1) {
   console.log("Current value of count = ", count);
}
```

You can perform any mathematical operation on the `count` variable that you want. Increment by 1, decrement by 5, multiply by 3, divide by 10... whatever you need for the problem you're trying to solve.

