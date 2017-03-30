# Student grades

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/the-static-web/grades && cd $_
touch index.html
touch grades.js
```

## Requirements

Loop over an array of student grades (values from 50-100) and output how many of each grades there are.

* A score of 50-60 is an F
* A score of 61-70 is a D
* A score of 71-80 is a C
* A score of 81-90 is a B
* A score of 91-100 is an A

Start with array of random scores in your JavaScript

```js
var scores = [82, 71, 95, 55, 98, 69, 72, 78, 84, 64, 58, 87];
```

Use `console.log()` to output the following criteria:

1. How many of each grade?
1. What is the lowest grade?
1. What is the highest grade?