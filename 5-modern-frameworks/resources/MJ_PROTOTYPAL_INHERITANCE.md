# Prototypal Inheritance and Composition

## is-a vs. has-a

Object inheritance is one way to build traits and behaviors into objects. The other, complementary way, is called [object composition](https://en.wikipedia.org/wiki/Object_composition). When you compose one object into another, they are allowed to evolve independently which helps create a more robust and flexible system. Using only inheritance to build more specialized objects results in fragile code with a very high refactoring cost.

Inheritance is used to describe an object at design/compile time, and composition is used to modify an object at run time.

Let's look at an example for a pizza order.

```js
var Order = function() {

};

var Pizza = function() {

};

var DeepDish = function() {

};

var ThinCrust = function() {

};

var Topping = function() {

};

var Pepperoni = function() {

};

var Mushroom = function() {

};

var Beverage = function() {

};

var Soda = function() {

};

var FruitPunch = function() {

};
```

With these basic functions set up, let's look at the possible `is-a` and `has-a` relationships. Start by asking simple questions about the relationship between two functions.

Is Soda a Pizza? No. Therefore, you're looking at a `has-a` relationship.

Is Mushroom a Topping? Yes. Therefore, you're looking at an `is-a` relationship.

Whenever you can answer the `is-a` question with yes, you can establish the prototype chain.

```js
var Topping = function() {

};

var Pepperoni = function() {

};
Pepperoni.prototype = new Topping();

var Mushroom = function() {

};
Mushroom.prototype = new Topping();
```

So in this case, we've established Topping as a root function in a prototype chain. But is it the only prototype chain? No. There's two more.

The Pizza prototype chain.

```js
var Pizza = function() {

};

var DeepDish = function() {

};
DeepDish.prototype = new Pizza();

var ThinCrust = function() {

};
ThinCrust.prototype = new Pizza();
```

The Beverage prototype chain.

```js
var Beverage = function() {

};

var Soda = function() {

};
Soda.prototype = new Beverage();

var FruitPunch = function() {

};
FruitPunch.prototype = new Beverage();
```

Now that we've set up the different prototype chains and established inheritance, we can start to use composition to build `has-a` relationships.

What can a Pizza have that isn't inherent to the Pizza itself? A Topping. So let's set up a property on a Pizza to hold the Toppings.

```js
var Pizza = function() {
  this.toppings = [];
};
```

Now, no matter what specific kind of Pizza you create - DeepDish or ThinCrust - there will be an array you can modify to add Toppings.

```js
// Create a Pizza
var gameDayPizza = new DeepDish();

// Create a Topping
var pepperoni = new Pepperoni();

// Add the Topping to the Pizza
gameDayPizza.toppings.push(pepperoni); // Now we have a pepperoni pizza
```

How about an Order? Is a Topping an Order? No.

Is a Pizza an Order? No.

Is a Beverage an Order? No.

This means that an order is composed of all the other types of objects. So we set up some default properties with `null` values that can be modified later by our application code.

```js
var Order = function() {
  this.pizza = null;
  this.beverage = null;
};

// Create an Order and add our Pizza to it
var gameDayOrder = new Order();
gameDayOrder.pizza = gameDayPizza;

// Create a Beverage and add it to the order
var pepsi = new Soda();
gameDayOrder.beverage = pepsi;

console.log("My game day order: ", gameDayOrder);
```

# External Resources

1. [Common Misconceptions About Inheritance in JavaScript](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a#.2le5vxm7w)
1. [JavaScript is object oriented](https://medium.com/just-javascript/javascript-is-object-oriented-a6f5e0f440f3#)
1. I am not covering the `class` feature of ES6 until it is fixed. Please do not use it until [it is fixed](https://medium.com/javascript-scene/how-to-fix-the-es6-class-keyword-2d42bb3f4caf#).
1. Great article titled [The Two Pillars of JavaScript](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3#.8a0kdyghs) which discusses the pitfalls of using `new`.
