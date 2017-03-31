# Music History 8

## Setup

### Create a new branch

`git checkout -b version8`

## Requirements

1. Use jQuery to retrieve the songs from your Firebase API.
1. Use jQuery to add new songs to your Firebase API with POST XHR calls.
1. Populate the form fields with data from your API.
1. When "Filter" button is pressed, update the song list with songs that only match the specified criteria.

Example:

```js
var filteredSongs = { songs: { } };

for (var key in existingSongObjectFromFirebase.songs) {
    var currentSong = existingSongObjectFromFirebase.songs[key];

    // Check if the currentSong.artist key value matches what the user selected
    // If it does, add the current song to the `filteredSongs.song` object
}

// Update the DOM with the filtered songs object
```

## Post promises requirements

These requirements only apply after we cover promises in class.

1. When you add, or delete, a song, the modules that perform the XHRs should return promises.
1. After the promise is resolved, you should display a [Bootstrap modal](http://getbootstrap.com/javascript/#modals) window to provide feedback on if the operation was successful, or not.

