# Counting Coins

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/the-static-web/coins && cd $_
touch index.html
touch coins.js
```

## Instructions

Write a program that will convert a dollar amount to the number of coins that make up the amount. Use the common American coins of quarters, dimes, nickels, and pennies.

```js
/*
  Input: 0.67
  Output:
  {
    quarters: 2,
    dimes: 1,
    nickels: 1,
    pennies: 2
  }

*/

function coinCounter () {
  // Initialize a JavaScript object to hold the coins
  var coinPurse = {};
  
  coinPurse.quarters = 0;

  return coinPurse;
}

var coins = coinCounter()
console.log();
```