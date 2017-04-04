# Music History Part 2

## Prerequisites

> :warning: This exercise requires that you have completed the [Music History 1](SW_MUSIC_HISTORY_01.md) exercise.

## Setup

1. Create a branch in your `musichistory` repository named `version-2`, and switch to that branch. `git checkout -b version-2` will create and switch you into that branch.

> This project is made up of several parts, and by creating a branch for each section you will be able to preserve the concepts you have learned on github as resources should you need them in the future. We have mentioned you should be commenting your code, right?

## Requirements

Use JavaScript arrays, loops, and innerHTML to show the music you love.

Use JavaScript to create a list of songs in the `index.html` file for your Music History project. Download the [`songs.js`](https://raw.githubusercontent.com/nashville-software-school/front-end-curriculum/9f5d7303f4c53102e8918f0ca06bebc84c91d266/resources/js-101.js) file, which contains an array of strings with song information.

1. Add one song to the beginning and the end of the array.
1. Loop over the array, and remove any words or characters that obviously don't belong.
1. Find and replace the `>` character in each item with a `-` character.
1. Add each string to the DOM in `index.html` in the main content area.

> **Example output:**  
>  
> {Song name} by {Artist} on the album {Album}  
>  
> {Song name} by {Artist} on the album {Album}  
>  
> ...
