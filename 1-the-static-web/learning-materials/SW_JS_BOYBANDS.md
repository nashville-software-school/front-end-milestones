# Boy bands and vegetables

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below, open a terminal window and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/the-static-web/boybands && cd $_
touch index.html
touch boybands.js
```

## Requirements

Paste the following code into the `<body>` of the HTML file.

```html
<div id="boy-bands">
</div>

<div id="vegetables">
</div>
```

Paste the following code into your JavaScript file.

```js
let bands = ["Boyz II Men", "NSync", "New Kids on the Block", "98 Degrees", "One Direction"];
let vegetables = ["Carrots", "Kale", "Zucchini", "Broccoli", "Squash"];

// The number of loops to perform (what if the array changes?)
let loopCount = 5;

// Keep track of which band we're on in the loop
let currentBand = "";

// Keep track of which veggie we're on in the loop
let currentVeggie = "";

// Get a reference to the appropriate DOM element for bands
let bandElement = document.getElementById(???);

// Get a reference to the appropriate DOM element for vegetables
let veggieElement = ???;

// Start looping
for (let loopTracker = 0; loopTracker < loopCount; loopTracker += 1) {
  
  // Add the band names into the correct <div>
  currentBand = ???;

  
  // Add the veggie names into the correct <div>
  currentVeggie = ???;

}
```


Loop through the two arrays provided (`bands` and `vegetables`) and output each element in the arrays into their corresponding HTML `<div>` element. Ensure that each item is in a block element (e.g. li, div, p. etc...)
