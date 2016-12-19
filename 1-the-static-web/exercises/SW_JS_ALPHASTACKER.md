# Alpha Stacker

## Instructions

For this exercise, you need to create a single JavaScript function named `stackLetters` that will use `console.log()` to print out letters in the alphabet to the browser console.

1. If you haven't done so yet, create the `workspace/exercises/alpha-stacker` directory structure in your home directory. Open your terminal and enter in the following command.

    ```
    mkdir -p ~/workspace/exercises/alpha-stacker
    ```

1. Now that you have created the directory, you want to change to that directory so that you can add files to it.

    ```
    cd ~/workspace/exercises/alpha-stacker
    ```

1. Create an `index.html` file with the [touch](http://www.linfo.org/touch.html) command.
1. Create an `alpha-stacker.js` file with the touch command.
1. Copy the following code and paste it into the `index.html` file. Notice that the `alpha-stacker.js` file is properly linked so that when you load this HTML file in a web browser, the logic in that file will be executed.

    ```
    <!DOCTYPE html>
    <html>
    <head>
        <title>Alpha Stacker</title>
    </head>
    <body>
    
        <script src="alpha-stacker.js"></script>
    </body>
    </html>
    ```

1. Open the `index.html` file in your web browser.
1. At this point, you will simply see a blank web page because you have no content in the HTML file. Open your developer tools using the *Option+Command+I* keyboard shortcut.
1. At the top of the developer tools panel, you will see the word *Console*. Click on that word. The `console.log()` statement will output any message into this panel in your developer tools. You can try it out immediately by clicking in the Console panel, and typing `console.log("Hello, world!")`, and then pressing your return key.

## Stacking Letters

Create a `stackLetters` function that should `console.log()` rows of letters. It should take an array containing the letters of the alphabet and output them in the developer console.

```
a
ab
abc
abcd
abcde
abcdef
etc...
```

> Starter code for alpha-stackers.js

```js
// Create an array that contains the letters of the alphabet
var alphabet = [];

// The stackLetter function should accept the array as the sole argument
function stackLetters (theAlphabetArray) {
    /*
      Write a `for` loop that iterates over the array argument and
      outputs the letters.
     */
}

// Invoke the function and pass in the array
stackLetters(alphabet)
```

## Adding Conditions to the Loop

Then add logic to `stackLetters` that places a space after every third letter. This will require you to do some basic math in JavaScript, and use an `if` statement.

Your job is to read the following English statement and write the equivalent in JavaSript code to make it work.

> If the current value of the [counter variable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for) can be evenly divided by 3 - using the JavaScript [remainder](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Remainder) operator - then add a single space to the output.

```
a
ab
abc
abc d
abc de
abc def
abc def g
abc def gh
abc def ghi
etc...
```