# Wide World Travel Guides

#### Part 1: Using a controller

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```
mkdir -p ~/workspace/exercises/rich-browser/wide-world-travel && cd $_
```

Create the following file structure:

```
world_wide_travel
 |_ app
 |    |_ controllers
 |    |     |_ bookCtrl.js
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

Add the follow data to `guides.json`. You will need to display all three pieces of information about each book, in any format you choose.
```
{
  "guides": [{
    "type": "city",
    "title": "Paris on $10 a Day",
    "price": 18.99
  }, {
    "type": "city",
    "title": "Venice: Canals and Stuff",
    "price": 14.50
  }, {
    "type": "city",
    "title": "Visiting Hoboken: Why?",
    "price": 1.25
  }, {
    "type": "country",
    "title": "Touring Brazil's Empty Olympic Stadiums",
    "price": 13.50
  }, {
    "type": "country",
    "title": "'Murica: Only Commies Travel Abroad",
    "price": 20.00
  }, {
    "type": "country",
    "title": "Australia: Every Animal Here Can Kill You",
    "price": 18.00
  }, {
    "type": "region",
    "title": "Backpacking Europe on Two Showers a Week",
    "price": 12.48
  }, {
    "type": "region",
    "title": "Rainforests of Cental America",
    "price": 15.00
  }, {
    "type": "region",
    "title": "The Evil Genius Guide to Taking over the Tri City Area",
    "price": 13.49
  }]
}
```
Remember to also add a `.gitignore` to the project root folder.

cd into `lib` and run `npm init` then install all of your dependencies for your task runner. Remember to use the `--save-dev` flag to add them to your `package.json` file.

Install Angular with `npm install angular`. Remember to add the script tag for angular to `index.html`.

Now you have the basic structure in place to display your book data in the DOM the Angular Way.

## Requirements

For this project you need to use Angular to list a collection of travel guides in the DOM.
Build an application that has one view, and one controller that will be responsible for retrieving the data and exposing it for use in the view. The view needs to list all book titles, which type of book it is, and the price for the book.

Fetch your data using an http call that returns a promise. Save the returned data as a property of the `$scope` object and loop through it to display the guidebook info to the user.

Here's a list of some things to include in your app in the appropriate spots:
+ Directives:
  + `ng-app="<your module name>"`
  + `ng-controller="bookCtrl"`
  + `ng-repeat="book in books"`
+ A call to the data folder for `guides.json` using `$http`
+ Use the `$q` service to wrap your http call in a promise
+ `$scope.books = <your array of guide books data>`
