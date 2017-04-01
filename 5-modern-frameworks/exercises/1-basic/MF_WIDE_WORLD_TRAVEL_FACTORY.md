# Wide World Travel Guides

#### Part 2: Adding a factory

## Prerequisite

> :warning: This exercise requires that you have completed the [Wide World Travel](./MF_WIDE_WORLD_TRAVEL.md) exercise.

## Setup

Add a `factories` directory to your existing file structure, and in that directory create a file named `guideFactory.js` to hold your new Angular factory module:

```
world_wide_travel
 |_ app
 |    |_ controllers
 |    |     |_ bookCtrl.js
 |    |
 |    |_factories
 |    |     |_ guideFactory.js
 |    |
 |    |_ app.js
 |
 |_ data
 |    |_ guides.json
 |
 |_ lib
 |    |_ gulpfile.js (or gruntfile.js)
 |
 |_ index.html
```

## Requirements

1. Make a new branch called `guide-factory`  
1. Separate the database interactions from the DOM interactions, and make your guidebook data available to your controller (and other, future controllers) by moving the http call for `guides.json` from `bookCtrl.js` into `guideFactory.js`
1. Inject your factory into `bookCtrl.js` as a dependency
