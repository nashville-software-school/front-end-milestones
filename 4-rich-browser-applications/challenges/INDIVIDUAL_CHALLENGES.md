# Individual Challenges

<a id="challenge-1"></a>
## Challenge \#1

Visit the [CSS3 Transitions, Transforms, Animation, Filters](http://css3.bradshawenterprises.com/) site and learn all about the cool stuff that the CSS3 specification gives web application developers. Using the techniques you discover there, develop your own way to transition between the different songs in your Music History song list.

<a id="challenge-2"></a>
## Challenge \#2

In Music History, set a background image for your page, and make sure that it takes up the full background of the page, no matter what size the viewport is.

<a id="challenge-3"></a>
## Challenge \#3

Sign up for a free account with [OAuth.io](http://oauth.io) and use their service to allow users to authenticate to your Music History application against any of the 150 providers they work with:  Facebook, Instagram, Twitter, Google,  Disqus, and many others.

<a id="challenge-4"></a>
## Challenge \#4

OAuth.io provides integration with [Stormpath](https://stormpath.com/), which allows you to have full user management for an application instead of relying upon another service like Google, Facebook, or Github to handle user authentication.

Sign up for a free Stormpath account, integrated with OAuth.io and then build a registration & login view for your application that lets user create a new account for use with your Music History.

<a id="challenge-5"></a>
## Challenge \#5

### Real Time Firebase DB
The Firebase API allows us to create a direct reference to a Firebase URL and attach an event handler that will execute code whenever anything changes at that location. Let's see how this works.

```js
// Create a reference to your Firebase database
firebase.initializeApp({
  apiKey: "apiKey",
  authDomain: "projectId.firebaseapp.com",
  databaseURL: "https://databaseName.firebaseio.com"
});

var firebaseBaseRef = firebase.database().ref();

// Listen for when anything changes on the "songs" key
myFirebaseRef.child("songs").on("value", function(snapshot) {

  // Store the entire songs key in a local variable
  var allSongsObject = snapshot.val();

  // Bind the allSongsObject to the song list Handlebar template

  // Bind the unique artists to the artists template

  // Bind the unique albums to the albums template

});
```

Once you get this working, click on one of the delete buttons, or add a new song, and the `on("value")` event will trigger immediately and your view of songs updates.
