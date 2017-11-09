# Temperature converter

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/the-static-web/converter && cd $_
touch index.html
touch converter.js
```

## Requirements

Write a program that will convert a temperature from fahrenheit to celsius, or from celsius to fahrenheit.

1. In the HTML, have one input field where someone can enter
  in a temperature.
2. Create a radio button group where Celsius or Fahrenheit 
  can be selected as the scale that the number should be 
  converted to.
3. Create a block level element that will hold the text of the
  converted temperature.
4. Create a button that, when clicked, displays the converted
  temperature.
5. Create another button that, when clicked, clears any text
  in the input field.
6. Add an event handler to the input field that checks if the 
  user pressed the enter key, and if that happens, perform
  the conversion.
7. If the temperature is greater than 90F/32C the color of 
  the converted temperature should be red.
8. If the temperature is less than 32F/0C the color of 
  the converted temperature should be blue.
9. For any other temperature, the color should be green.

```js
function toCelsius () {

}

function toFahrenheit () {

}

// Get a reference to the button element in the DOM
var button = document.getElementById("converter");

// This function should determine which conversion should
// happen based on which radio button is selected.
function determineConverter (clickEvent) {
  console.log("event", clickEvent);
}

// Assign a function to be executed when the button is clicked
button.addEventListener("click", determineConverter);
```
