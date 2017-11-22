# AngularJS 105

## Custom directives

A directive, at its most simple implementation, is simply a fancy `ng-include`. Check out the custom directive below.

```js
app.directive("simpleDirective", function() {
  return {
    restrict: "E",
    templateUrl: "partials/song-brief.html"
  }
});
```

Now you can use a custom DOM element to load the contents of `song-brief.html` in any other partial.

```html
<div>
  <simple-directive></simple-directive> <!-- Contents of song-brief.html will go here -->
</div>
```

Let's look at a more powerful example of what directives can do for your code. Beyond being a way to include DOM anywhere in your code, which is itself a great feature, your directive can provide complex functionality based on attributes that are defined on the custom element.

So let's start with the `song-brief` partial. This is the base DOM of our directive. It displays the artist and album name for each song, but also will show stars, based on the `rating` key on each song object. Here's a sample JSON representation of a song.  Change the songs in your json files to match this structure.

```js
{
  "id": 0,
  "name": "Song",
  "artist": "Artist",
  "album": {
    "year": 2010,
    "name": "Album"
  },
  "rating": 3
}
```

##### **File:** partials/song-brief.html

```html
<section class="text--small">
  <div>
    By {{ selectedSong.artist }} on {{ selectedSong.album.name }}
    <ul class="rating">
      <li class="{{star.class}} star" ng-repeat="star in stars">&#9733;</li>
    </ul>
  </div>
</section>
```

Notice that there is an `ng-repeat` for a `stars` property on the object, but that key does not exist in the raw JSON. The directive adds the `stars` key in its own scope for use in rendering the directive. Let's look at how it does that.

##### **File:** app/directives/song-directive.js
```js
app.directive('songBrief', function() {
  return {
    restrict: "E", // Restrict directive to element
    scope: {
      selectedSong: "=song",  // Bind the `song` attribute in the DOM
                              // to the selectedSong locally scoped variable
      maxRating: "=" // Bind `max-rating` to maxRating local variable
    },
    templateUrl: "partials/song-brief.html",
    link: function(scope, elem, attrs) {

      /*
        Create a new key on the song called `stars`. It's
        an array of objects. Each object contains which
        class to use on each of the stars.
       */
      function setStars() {
        scope.stars = [];
        var rating = parseInt(scope.selectedSong.rating);
        for (var i = 0; i < scope.maxRating; i++) {
          var clazz = (rating <= i) ? "star--empty" : "star--filled";
          scope.stars.push({class: clazz});
        }
      }

      /*
        Since the selectedSong in the `song-view` template
        is bound directly to an object in the controller
        that gets updated after an XHR, I have to watch that
        variable for changes and then run the logic again
        once it gets updated values.
       */
      scope.$watch('selectedSong', function(value){
        console.log("value changed");
        scope.selectedSong = value;
        setStars();
      });

      setStars();
    }
  };
});
```
Next lets add a little CSS to make our stars look better.  Create a styles/main.css file and add the link tag to your index.html.  Then add the following:

```css
.rating{
  list-style: none;
}

.star--empty{
  color: gray;
}
.star--filled{
  color: yellow;
}

.star{
  display: inline-block;
}
```

Now you can include the custom directive in other partials.  Replace the contents of your song-list.html file with the following:

##### **File:** partials/song-list.html

```html
<section>
  <div>
    <input type="text" ng-model="songSearchText" />
  </div>

  <div class="c-song" ng-repeat="song in songs | filter: songSearchText">
    <a href="#!/songs/{{ song.id }}">{{ song.name }}</span></a>
    <song-brief song="song" max-rating="5"></song-brief>
  </div>

  <a href="#!/songs/new">Create New Song</a>
</section>
```

