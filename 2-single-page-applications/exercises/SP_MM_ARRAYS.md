# Very Large Array - Muscle Memory Exercise

## Prerequisite
Students should have [music history 3](SP_JS_MUSIC_HISTORY_3.md) completed before attempting this muscle memory exercise.

## Setup

1. Create a branch in your `musichistory` repository named `MM-arrays`.
1. Switch to that branch.

## Requirements

`Muscle memory exercises are meant to improve your muscle memory for important javascript concepts. While doing these exercises try to minimize, if not eliminate copying and pasting.`

Use JavaScript arrays and innerHTML to show the music you love.

Students must use JavaScript to create arrays, modify them (using only the following methods: join, push, reverse, sort, concat and unshift), and output lists to the DOM.

1. Each student must create three separate arrays, one for songs, one for albums, and one for artists.
1. The song array should be initialized with 10 songs.
1. Each subsequent array should hold the corresponding data (artist and album).
    - For this exercise make sure each song is from a unique artist and album. We will deal with multiples in a later exercise
1. An output should be added on the add song page, under the form, for each of the sections (songs, artists & albums).
1. Each output section should have some sort of title or headline before it.
1. Add 2 more songs from the add song form.
    + Each song should be added to the end of the song array.
    + Each artist should be added to the beginning of the artist array.
    + Each album should be added to the end of the album array.
1. For each output element arrange the corresponding data as follows:
    *   Output vertically descending alphabetically.
    *   Output vertically ascending alphabetically.
    *   Output vertically exactly as the data was added.
    *   Output vertically exactly as the data was added, inverted.
    *   Output horizontally descending alphabetically, separated by `, `.
    *   Output horizontally ascending alphabetically, separated by ` >> `.
    *   Output horizontally exactly as the data was added, separated by ` : `.
    *   Output horizontally exactly as the data was added, inverted, separated by ` | `.
1. Each output area should be separated by a headline tag.

#### Bonus
*   Handle both upper and lowercase inputs. The way this is accomplished is up to the student. Additional array methods may have to be employed to complete this bonus item.


## Merging your branch

After you've got all of the requirements completed, follow these steps.

1. In your `musichistory` directory, enter the command `git checkout master`. This switches you back to the master branch.
1. `git merge -X theirs MM-arrays`
1. If you see a vim screen with a default message in it just `:x` to save and exit.

Your branch is now merged into the master branch and you can push the master branch up to Github with `git push origin master`.