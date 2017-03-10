# Javascript Functions

What is a function? Not even considering software, what does the word function mean to you? Consider the following sentences.

> The function of an oven is to cook food. You put cold, uncooked food into an oven at 450 degrees, and after 20 minutes passes, delicious, cooked food comes out.

Modern programming languages make it fairly easy to express this in code. Let's look at how we could write the same thing in JavaScript.

```js
function oven (uncooked_food) {
  const temperature = "450";
  const time = "20";
  const cooked_delicious_food = uncooked_food + (temperature * time);

  return cooked_delicious_food;
}
```

That JavaScript code defines a function. The name of the function is `oven`, and the code inside it performs the task of cooking the uncooked food. The `uncooked_food` variable in the parenthesis is what you put in the oven. In JavaScript, these are called function arguments. The `return` statement specifies what comes out of the oven.

At this point, we have a design for an oven. The next step is to actually use the oven. To use a JavaScript function, you simply type its name followed by parenthesis.

```js
oven()
```

This is called invoking the function.

Now, let's put uncooked food into the oven by passing a string value into it.

```js
oven("raw fish");
```

By putting the string of "raw fish" into the oven function, the `uncooked_food` argument now has a value. The last part of the process is to take out the cooked food. Since the function used the `return` statement, we can stored that returned value in a variable.

```js
const cooked_fish = oven("raw fish");
console.log(cooked_fish);
// raw fish9000
```

You can try this out in Chrome. Press `Alt+Cmd+I` to open the Chrome development tools. At the top, click the section titled *Console*. Copy the `oven` function into the console, then press `Return`.

Next, paste the following code, change the food to whatever you want.

```js
const cooked_fish = oven("some other food");
```

Then type `cooked_fish` to see what its value is.

![animation](./Met0ECu9qp.gif)

At the most basic, a function is a bit of code that performs a specific task. That task can be performed as many times as you want, based on the needs of your application.

```js
// Cook dinner
const cooked_chicken = oven("raw chicken");
const roasted_broccoli = oven("broccoli");

// Bake dessert
const baked_cake = oven("cake batter");
```

### Function Side-Effects

Not all functions need to return a value. Let's look at an example of a function that simply performs a specific task and ends.

```js
/* 
  This function adds two numbers together and outputs
  the result in the console.
*/
function update_dom (dom_element, content) {
  dom_element.innerHTML = dom_element.innerHTML + content;
}
```

That's a perfectly fine JavaScript function. In a more complicated JavaScript application, like the ones you will be building in groups here at NSS, you will build functions that perform a complex task so that you don't have duplicated code through your project.

What the function does have is a side effect because its logic affects the DOM rather than just producing a consistent return value each time it is called. Therefore, it's not a [pure function](#pure-functions).

# Higher Order Functions

Functions that operate on other functions, either by taking them as arguments or by returning them, are called *higher-order functions*.

Since functions are objects, you can pass them as arguments to other function, just like you would any other native JavaScript type. In the previous example for our `oven`, we passed a string value into the over, and got a string value back out of the oven.

There's more to a meal than cooking the food in an oven. We first need to prepare the meal, and after it is cooked, we need to serve it. We also need to decide if the dish is going to be baked or broiled.

Let's define a function for each purpose.

```js
/* 
  The ellipses (...) will take ALL arguments and make 
  an array out of them, stored in the ingredients argument
*/
function prepare_food (...ingredients) {
  const chopped = ingredients.map(ingredient => {
    return `10 slices of ${ingredient}`;
  });

  return chopped;
}

function bake (raw_dish) {
  return `Baked [${raw_dish}]`;
}

function broil (raw_dish) {
  return `Broiled [${raw_dish}]`;
}

/* 
  The `type_of_cooking` argument will hold a function
  reference. This makes `cook_food` a higher-order
  function.
*/
function cook_food (raw_dish, type_of_cooking) {
  // We invoke the specific cooking function here
  const result_of_cooking = type_of_cooking(raw_dish);
  return result_of_cooking;
}

function serve_food (cooked_dish, container) {
  return `A ${container} of ${cooked_dish} is on the table`;
}

// Prepare the ingredients
let raw_dish = prepare_food("onion", "carrot", "zucchini");

// Cook the raw ingredients
let cooked = cook_food(raw_dish, bake);

// Serve the cooked dish in a container of your choosing
let menu_item = serve_food(cooked, "platter");
```

## Pure Functions

> In computer programming, a function may be considered a pure function if both of the following statements about the function hold:
> 
> 1. The function always evaluates the same result value given the same argument value(s). The function result value cannot depend on any hidden information or state that may change while program execution proceeds or between different executions of the program, nor can it depend on any external input from I/O devices (usually—see below).
> 2. Evaluation of the result does not cause any semantically observable side effect or output, such as mutation of mutable objects or output to I/O devices.
>
> Source: [Wikipedia](https://en.wikipedia.org/wiki/Pure_function)

```js
// Pure function
function add (first, second) {
  return first + second;
}

// Impure function
function dice_roll (sides) {
  return Math.floor(Math.random() * sides) + 1;
}

// Pure function
function full_name (first_name, last_name) {
  return `${first_name} ${last_name}`;
}

// Impure function
function update_dom (dom_element, content) {
  dom_element.innerHTML = dom_element.innerHTML + content;
}
```