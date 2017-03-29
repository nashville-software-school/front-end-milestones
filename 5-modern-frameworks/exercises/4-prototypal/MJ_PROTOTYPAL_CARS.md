# Car Manufactory

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/mjd/cars && cd $_
```

## Instructions

Follow the instructions in the comments below.

##### manufactory.js

```js
/*
  Create a function named Car with one property named `manufactured_date`
  whose value will be Date.now()
 */
function Car () {
  // Create the manufactured date property (see above)
}

/*
  1. Create a new constructor function for the make of your favorite car.
  2. It must inherit from the more general Car object.
  3. Give it one property, named manufacturer, that holds a string value. 
         For, example, this.manufacturer = "Ford".
 */
function YourFavoriteMake () {
  // Define the manufacturer instance variable
}
// Set the prototype to a new Car instance


/*
  1. Create a constructor function named after your favorite car model.
  2. It must inherit from the specific make type you created in previous step.
  3. Create some instance properties that are specific to the specific
        car model (e.g. horsepower, cargo capacity, etc.)
*/
function YourFavoriteModel () {

}
// Set the prototype to appropriate model you created above and set the model name argument
YourFavoriteModel.prototype = new ???;

/*
    Being an avid car collector, you own three different cars all of
    same model from your favorite manufacturer.
    
    1. Create three new instances of your favorite car.
    2. Create a new property on each object to hold the license plate
       number for each car.
*/
var myFirstFavoriteCar = new ???;
myFirstFavoriteCar.plate_number = "";
...


/*
  Now let's see some power of prototypal inheritance. Create a function for
  another model that's made by the manufacturer as your previous car. So if
  your first model was Fusion, make another one here for F150, for example.
 */
function AnotherModel () {

}
/*
  Assign the prototype to the make you define above. Now both models will
  inherit the `manufacturer` property from the make function.
 */



/*
  Now create an instance of this new car model to put in your garage. Remember
  to give it a plate number.
 */
```

