>Linking objects together to share properties and delegate behavior
# Javascript: Introduction to Objects

The most basic object is a collection of key:value pairs surrounded by curly braces.

```js
let myCar = {
  make: "Nissan",
  model: "Xterra",
  year: 2006,
  color: blue
}
```

You can add new key:value pairs after the initial definition.

```js
myCar.doors = 4;
myCar.sunroof = false;
```

You can then access the value of any of those keys.

```js
console.log("My car has " + myCar.doors + " doors.");
```

However, ES5 introduced a new way to create objects. The following creates an empty object with a null prototype.

```js
let nissan = Object.create(null);
```

You can add a property to the object the same way as before.

```js
nissan.make = "Nissan";
```

You can also create objects that inherit from other objects.

```js
let myNissan = Object.create(nissan);
```

You can then access the prototype's properties on the new object.

```js
console.log("My car is a " + myNissan.make + ".")
```

# Greeting Card Maker
The existing `CardMaker` object below contains a single method that returns a greeting. Your job is to add one or more methods to it, then use it as a prototype for at least three other objects using `Object.create()`

## Minimum requirement
Each new object should represent a different type of greeting card, such as birthday or Valentine's Day, with its own unique properties. Output two messages, one from the front and one from the inside of the card, to the console. 

## Challenges 
+ Make additional objects that allow more specific card types, such as children's birthday and adult's birthday,
that inherit from a `BirthdayCard` object.
+ Output the HTML strings with classes to the DOM that you can style with CSS. 
+ Refactor "makeFrontMessage" to return something more elaborate. 

```
const CardMaker = {
  makeFrontMessage: function(string) {
    return `<h2>${string}</h2>`
  }
}

//Refactor this to link this object to cardMaker
const BirthdayCard = Object.create();
```
