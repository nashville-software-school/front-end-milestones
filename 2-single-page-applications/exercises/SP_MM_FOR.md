# For The Love Of Loops - Muscle Memory Exercise

## Prerequisite
Students should have [Very Large Array](SP_MM_ARRAYS.md) completed before attempting this muscle memory exercise.

## Setup

1. Create a branch in your `musichistory` repository named `MM-for`.
1. Switch to that branch.

## Requirements

`Muscle memory exercises are meant to improve your muscle memory for important javascript concepts. While doing these exercises try to minimize, if not eliminate copying and pasting.`

Use JavaScript arrays and innerHTML to show the music you love.

Students must use JavaScript to create arrays, modify them (using only for loops), and output lists to the DOM.

1. Using the three separate arrays you created in the Very Large Array exercise code the following functionality.
1. Using the output elements from the previous muscle memory exercise, utilize for loops to duplicate output to the DOM.
1. For each output element send the corresponding data as follows:
    *   Output vertically descending alphabetically.
    *   Output vertically ascending alphabetically.
    *   Output vertically exactly as they were added.
    *   Output vertically exactly as they were added, inverted.
    *   Output horizontally descending alphabetically, separated by `, `.
    *   Output horizontally ascending alphabetically, separated by ` >> `.
    *   Output horizontally exactly as they were added, separated by ` : `.
    *   Output horizontally exactly as they were added, inverted, separated by ` | `.
1. Add a couple of songs in the add song form and make sure your loop logic works.
    -   For this exercise make sure each song is from a unique artist and album. We will deal with multiples in a later exercise

#### Bonus
*   Handle both upper and lowercase inputs. The way this is accomplished is up to the student. Additional array methods may have to be employed to complete this bonus item.
*   Try to output each section using just one for loop for each section.
*   Try to achieve the same results using just one for loop for all three sections.
*   Handle extra punctuation at the end of a list.


## Merging your branch

After you've got all of the requirements completed, follow these steps.

1. In your `musichistory` directory, enter the command `git checkout master`. This switches you back to the master branch.
1. `git merge -X theirs MM-for`
1. If you see a vim screen with a default message in it just `:x` to save and exit.

Your branch is now merged into the master branch and you can push the master branch up to Github with `git push origin master`.