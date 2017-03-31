# Music History Part 6

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
cd ~/workspace/musichistory
git checkout -b version-6
```

## Instructions

Now is the time to make Music History a fully functional, single page, modular, asychronous, application.

### Modular with Browserify

1. Using Browerify, you should create several modules for the application.
1. One module is responsible for loading songs from a JSON file and storing them in an array. This module should expose one method for getting the entire list of songs, and one method for adding a song to the array.
1. One module is responsible for making the filtering form work. Therefore, it will need to use methods from the previous module.
1. One module is responsible for showing the two views of the app (song list and song form).

### Filtering

1. When the user selects an artist, only songs from that artist should appear.
1. When the user selects an album, only songs from that album should appear.

### Adding Songs

1. The new music form should have a field for every key on a song object. We started with just Artist, Album, and Title, but you can add more if you wish.
1. The music form should be fully functional. When you click the *Save Song* button, a new object should be added to the array of songs. The DOM should also be immediately updated with the new song added.