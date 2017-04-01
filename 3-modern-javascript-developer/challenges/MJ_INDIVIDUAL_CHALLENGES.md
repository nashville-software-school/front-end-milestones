<a id="challenge-1"></a>
# Individual Challenge \#1

## Checkers using jQuery

### Setup
These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/mjd/checkers && cd $_
```

1. Use `npm` to install jQuery, Browserify, and any other packages you need to compile your modules.

### Instructions
Create a checkers game using only jQuery to manipulate the DOM. Augment your javascript files using Browserify. You should have a minimum of three javascript files that handle aspects of the game. Create at least two object constructors, one named Game and one named Player that will utilize methods and properties from your augmented files.

### Requirements

1. Create a grid of sixty-four boxes
1. Alternate colors of the boxes
1. Initialize the board with 12 pieces on either side
1. Only one side may move at a time
1. To move a piece you can drag and drop
1. Moves must comply with the following rules:
    1. Pieces may only move diagonally towards opponent
    1. Pieces may move only one square (unless capturing)
    1. When a piece is jumped it is removed from the board
    1. Allow for multiple jumps
    1. If piece is in a position to capture it must make the move (if more than one capture is available the player may choose)
    1. When a piece reaches the furthest row from the player it becomes a king
    1. Kings may move forward and backwards
    1. Kings may combine captures forward and backwards
    1. A player wins when their opponent can no longer make a move
1. When a win happens:
    1. Alert the players who won
    1. Disallow any further clicks on the game board
    1. Display a `play again` button that resets the game

*Bonus* Save game stats and output them when a player wins.



<a id="challenge-2"></a>
# Individual Challenge \#2

For the truly brave.

Develop a process that lets you automate the running of your unit tests with a Grunt task. You could start by looking at the [grunt--contrib-jasmine](https://www.npmjs.com/package/grunt-contrib-jasmine) npm package. You'll need Browserify and a few other tools in order to get it working. It will require a lot of Googling and reading articles because it is **not** a straightforward, or easy, task.  

This article may prove helpful:
[Testing a Browserify Project With Jasmine and Grunt](http://dapperdeveloper.com/2015/01/21/testing-a-browserify-project-with-jasmine-and-grunt/)

<a id="challenge-3"></a>
# Individual Challenge \#3

## Cutting edge prototypal inheritance & composition

Pick any exercise or group project that you've completed so far and use `Object.create()` instead of the `new` keyword to create objects and establish prototype chains.

### Resources

1. [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create) entry on `Object.create()`
1. [Video intro](https://www.youtube.com/watch?v=giJV6boOLxU) to using `Object.create()` for inheritance
1. I am not covering the `class` feature of ES6 until it is fixed. Please do not use it until [it is fixed](https://medium.com/javascript-scene/how-to-fix-the-es6-class-keyword-2d42bb3f4caf#).
1. Great article titled [The Two Pillars of JavaScript](https://medium.com/javascript-scene/the-two-pillars-of-javascript-ee6f3281e7f3#.8a0kdyghs) which discusses the pitfalls of using `new`.