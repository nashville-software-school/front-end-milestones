# Create Your Own Zoo

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/mjd/zoo && cd $_
```

## Instructions

Create a three level prototype chain for identifying animals. Pick a couple of your favorite animals, and research their species and the genus that the species belongs to. Wikipedia is a great resource for this.

1. Create a base `Animals` function.
1. Create a genus function for each of your favorite animals that inherits from `Animal`.
1. Create a species function for each of your favorite animals that inherits from the appropriate genus.
1. Every animal must have a name property.
1. Each genus must have a `genusName` property.
1. Each species must have a `speciesName` property.

##### example.js

```js
function Animal () {

}

function Tenodera () {
  this.genusName = null;
}
// Set Animal as the prototype of Tenodera

function TenoderaSinensis () {
  this.speciesName = null;
}
// Set Tenodera as the prototype for TenoderaSinensis

// Create a new instance of TenoderaSinensis

// Output the name, genus name, and species name for your TenoderaSinensis
```

Once you get a couple animals done, and you feel you are comfortable with the mechanism for inheritance, add some more genus and species functions.