## Firebase

Firebase allows you to upload data to a remote server and then use an API to perform CRUD (Create, Read, Update, Destroy) actions on that data.

To quickly get up and running with some data to experiement with, you can import a JSON file into your Firebase. This format -- an object with a single property that an object of objects -- allows you to save related data in a 'collection'. This way, if we also wanted to save some information about albums, artists, genres, etc, each of those could be saved in their own collections.  

Firebase will store items in this same format even when you start saving things directly to it with XHRs. The difference will be that instead of having to add keys to every object yourself, like "songSharp", Firebase will autogenerate a key as a unique identifier that will look something like this: `-KXw6pl9XZRGYaX4vLzJ`. That's good, since naming things is hard, and naming things accidentally the same thing is too easy. 

```
{
  "songs": {
    "songSharp": {
      "name": "Sharp Dressed Man",
      "artist": "ZZ Top",
      "album": "Eliminator"
    },
    "songBreakfast": {
      "name": "Breakfast in America",
      "artist": "Supertramp",
      "album": "Breakfast in America"
    },
    "songGoodbye": {
      "name": "Goodbye Mary",
      "artist": "Supertramp",
      "album": "Breakfast in America"
    },
    "songCarry": {
      "name": "Carry on My Wayward Son",
      "artist": "Kansas",
      "album": "Overture"
    },
    "songGimme": {
      "name":"Gimme All Your Lovin",
      "album": "Eliminator",
      "artist": "ZZ Top"
    },
    "songJungle": {
      "name":"Welcome To The Jungle",
      "album": "Appetite For Destruction",
      "artist": "Guns & Roses"
    },
    "songRather": {
      "name":"Rather Be",
      "album": "Rather Be",
      "artist": "Silent Bandit"
    },
    "songWalk": {
      "name":"The Walk",
      "album": "How Do You Do",
      "artist": "Mayer Hawthorne"
    }
  }
}
```

### Firebase via XHR calls

#### GET

To start off, all we're going to do is change how we get our data. Use your latest version of Music History as an example. Since we've imported it all into Firebase, all you need to do is open your `populate-data.js` file and change the URL. Right now, it's pointing to a local `songs.json` file, but you're going to change it.

1. Go to your Firebase console in Chrome and copy the URL.
2. Update the `url` property in your XHR to `<url you just copied>/.json`. (That `.json` is important)
3. Refresh your page.

Since your existing code is already set up to handle a data object with a `songs` key on it, everything should just work normally. You've simply changed the location of where the data lives... nothing else changes.

#### POST

Next, we get to use the real power of databases, XHRs and APIs. Up until now, your Add Song form didn't really do anything. Once you refreshed the page, your new song disappeared. Not any more.

Create a new module in your application - let's name it `save-song.js` - and we're going to use the POST method to add a song. In a POST, you need to actually send the data to the server, and with a jQuery AJAX call, we specify a `data` key in the config object.

```js
define(["jquery"], function($) {

  // Define your event listener for the add song button
  $("#add-song").click(function() {
    // Extract all the form field values and create a new song object with them
    var newSong = {
      artist: "",
      album: "",
      title: ""
    };

    // POST the data to Firebase
    $.ajax({
      url: "<your-firebase-url>/songs/.json",
      method: "POST",
      data: JSON.stringify(newSong)
    })
    .done(function(response) {
      console.log("response from Firebase:", response);
      // You'll likely want to execute the code that you're using
      // on page load here to run the GET XHR and bind to Handlebars
    });
  });
});
```

#### DELETE

Now it's time to delete a song. In your Handlebars file, add a `<button>` element for each song, labeled "Delete". Add a class of `delete-button` to each one. Remember that dynamically added DOM elements have to have events handled at the document level.

Create a new module in your application named `delete-song.js`.

```js
define(["jquery"], function($) {

  $(document).on("click", ".delete-button", function() {
    var songKey = $(this).attr("id");

    // DELETE the song from Firebase by specifying the URL to
    // the exact song you are targeting.
    $.ajax({
      url: `<your-firebase-url>/songs${songKey}/.json`,
      method: "DELETE"
    })
    .done(function(response) {
      console.log("response from Firebase:", response);
      // You'll likely want to execute the code that you're using
      // on page load here to run the GET XHR and bind to Handlebars
    });
  });

});
```

Now all you have to do is use the special `{{@key}}` decorator in your Handlebar file to set the song's key as the delete button's `id` attribute. If this is your first exposure to `{{@key}}`, be sure to read the Handlebars docs to understand what it does.


> **Pro tip:** Ever need to convert an object collection into an array of objects, and maintain the original key names for each object?
>
> ```js
> var arr = Object.keys( x.songs ).map( function( key ){
>   var newArrItem = x.songs[ key ];
>   newArrItem.key = key;
>   return newArrItem;
> });
> ```
