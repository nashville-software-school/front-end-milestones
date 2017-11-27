# Sandwich Maker

## Setup

These commands are a helpful quick start. You may choose to ignore them
completely and create your own directory structure. If you choose to use this
recommendation, just copy the commands below and paste. It doesn't matter what
directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/spa/sandwich && cd $_
touch index.html
mkdir javascripts && cd javascripts
touch SandwichMaker.js
```

## Requirements

Your project should have one HTML file that has:

* A section of options for each sandwich part
* The ability to select multiple, or zero, choices for each section (such as
  turkey _and_ bacon, or "no meat")
* An empty DOM element into which the final sandwich order and its cost will be
  inserted

Create a sandwich order form that allows the user to select all the ingredients
for a custom deli sandwich. Create a `Sandwich` module, then create the
following as individual modules.

* bread
* meat
* cheese
* condiments
* veggies

The ingredient choices in each module should be stored as JS objects that
contain the ingredients as keys and their cost as the value. `{"turkey": 0.90,
"bacon": 1.50}`

Make sure the ingredient objects cannot be accessed by the other modules except
through an accessor (getter) method.

Each module should expose, via `module.exports`, a method named
`add{ingredient}` (e.g. `addMeat` or `addVeggies`) that accepts a single
argument. That argument's value should be the ingredient selected by the user.
You will need to implement Browserify as a task in a Gruntfile, in order to
compile your modules into a single JS file.

You should also create an additional JavaScript file that handles interacting
with the form elements and determining which method should be called.

> Don't worry about exposing the prices to the user until you display the final
> cost. This is just an exercise, not a business model.

Here's some simple boilerplate code to get you started.

##### meat.js

```js
// if you cannot answer the questions in the example, do not copy and paste it. Know what's going on before you use code you didn't write

// Private variable to store the different meat prices. How is it private?
let meatPrices = { salami: 0.75, "roast beef": 1.25 }; //why is one key in quotes but the other isn't?

const addMeat = function(meatSelection) {
  //code that grabs the correct meat price and returns it
};

module.exports = { addMeat }; //What exactly is being exported here?
```

##### DOMHandler.js

```js
// pull in the module(s) you'll need to fetch the toppings' prices
const meat = require("./toppings/meat"); //If this is the path to your mat.js file, how do you need to structure your files to make this work?

// Variable to hold the price of the sandwich. Default to 0.
var sandwichPrice = 0;

// Variable to hold topping that the user selects
var selectedTopping;

// Get a reference to the <select> element that has all the meat options
var meatChooser = document.getElementById("meat-chooser");

/*
  A <select> element broadcasts a change event, so you listen for it
  and get the value of the topping from your augmented IIFE
*/
meatChooser.addEventListener("change", function(event) {
  // Get the value chosen from the DOM
  selectedTopping = event.target.value;

  // Determine the price of the topping chosen

  // Add the price to the total price and update the DOM to display the sandwich cost
});
```

### Bonus

Once you have this working, refactor it by adding an additional module that acts
as a control center of sorts for all of the toppings modules. Then import that
single module into `DOMHandler.js`. What would be the advantage of doing this?
Isn't it just more code to achieve the same result? Look into the concept of
abstraction in software design and decide if this fits that definition.
