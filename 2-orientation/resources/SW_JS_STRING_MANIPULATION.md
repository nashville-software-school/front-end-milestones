# Javascript: String manipulation

### Joining two strings together
It's called concatenation.
```
var firstName = "Michael";
var lastName = "Corleone";
var fullName = firstName + " " + lastName;

alert(fullName);
```

In JavaScript, the `+` character not only adds two numbers together, but it also concatenates strings

### How long is it?
```
var phrase = "How much wood would a woodchuck chuck if a woodchuck could chuck wood";
alert(phrase.length);
```
### Finding characters in a string
You use the `indexOf()` method that is automatically added to any variable that holds a string value.

```js
var phrase = "The quick brown fox jumps over the lazy dog.";

// In JavaScript, the first position of a string 
// (called the index) is actually 0, not 1. The 
// same is true in arrays.
alert(phrase.indexOf("T"));

alert(phrase.indexOf("x"));
```

### Determine which character is at a position in a string
Yo use the `charAt()` method that is automatically added to any variable that holds a string value.

```js
var phrase = "How now brown cow?";
var position = phrase.charAt(8);
alert(position); // Will alert "b"
```

### Replacing characters in a string
You use the `replace()` method that is automatically added to any variable that holds a string value.

```js
var phrase = "The lazy dog";
var newPhrase = phrase.replace("lazy", "bounding");
alert(newPhrase);
```

Change every occurrence by using a regular expression. Try this out.

```js
var phrase = "The lazy dog likes the weird fox";
var newPhrase = phrase.replace(/o/g, "i");
alert(newPhrase);
```

### Converting strings to numbers

```js
var five = "5"; // "5"
var numberFive = parseInt(five); // 5
```

## Adding strings to your web page

Learn to use `document.getElementById()` and  `element.innerHTML` to add text to a web page with JavaScript. This is an alternative to `document.write()` which is taught in the Treehouse video for their first JavaScript program.

##### **Example**
---
```html
<div id="container">

</div>
```

```javascript
var phrase = "Hey, look at me!";
var element = document.getElementById("container");
element.innerHTML = phrase;
```