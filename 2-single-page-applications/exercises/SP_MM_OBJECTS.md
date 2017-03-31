# Objective Reasoning - Muscle Memory Exercise

## Prerequisite
Students should have [Music History 4](SP_JS_MUSIC_HISTORY_4.md) & [For The Love Of Loops](SP_MM_FOR.md) completed before attempting this muscle memory exercise.

## Setup

1. Create a branch in your `musichistory` repository named `MM-objects`.
1. Switch to that branch.

## Requirements

`Muscle memory exercises are meant to improve your muscle memory for important javascript concepts. While doing these exercises try to minimize, if not eliminate copying and pasting.`

Use JavaScript objects, for loops and innerHTML to show the music you love.

Students must use JavaScript to filter objects, modify them, and output lists to the DOM. Use the three separate arrays created in the Very Large Array exercise to build objects.

1. Create a new empty array called `songObjects`.
1. For each song in your previous song title array create an object that includes the song title, artist, album and genre.
1. Add a genre input to the add song section in the `index.html` file.
1. When a song is added it shoud be added not only to the DOM but to the array of objects as well.
1. Write a function that uses a for loop to populate the DOM on the add song section as follows:

    >  Song Title  
    >  Artist  
    >  Album  
    >  Genre  

1. Write four more functions that use for loops to populate the DOM on the add song section for each of the four categories (song title, artist, album & genre).

#### Bonus
*   Refactor your code to accomplish the same results using only one function and one for loop.


## Merging your branch

After you've got all of the requirements completed, follow these steps.

1. In your `musichistory` directory, enter the command `git checkout master`. This switches you back to the master branch.
1. `git merge -X theirs MM-objects`
1. If you see a vim screen with a default message in it just `:x` to save and exit.

Your branch is now merged into the master branch and you can push the master branch up to Github with `git push origin master`.