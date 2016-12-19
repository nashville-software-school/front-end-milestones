# Language Translator

## Setup

```bash
mkdir -p ~/workspace/group-projects/translator && cd $_
```

This will be a group project managed by Github Classroom, so pick one teammate to create the Classroom team. Once the repo is created, run the initialization commands that create the inital README and push the branch up.

At that point, the other teammates can join the Classroom team and clone the repository.

## Instructions

Represent a small bilingual lexicon as a Javascript object (see example below) and use it to translate a holiday card message from English into another language. Each member of the team will build a JavaScript module that will convert text entered into an input field to the language that they choose.

`{"merry":"god", "christmas":"jul", "and":"och", "happy":"gott", "new":"nytt", "year":"år"}`

This is Swedish, so please choose other languages. You can add as many words/translations as you wish so that the user can write more complex holiday cards.

1. One team member creates a Github project and adds the others as collaborators.
1. Each team member picks a language.
1. Your project should have one HTML file that has a textarea, a select element with an option for each language, a button with a label of "Translate", and an empty DOM element into which the translated text will be inserted.
1. The team must discuss and choose a single variable name that will hold all of the logic that the team creates (i.e. see the Sedan example above).
1. Each team member will create one JavaScript file that contains one IIFE. Each teammate's IIFE will augment the other teammates' IIFEs.
1. The lexicon should be a private variable that cannot be accessed by the other team member's module except through an accessor (getter) method.
1. Each IIFE should expose, in its public interface, a method named `translateTo{Language}` (e.g. `translateToSpanish` or `translateToFinnish`) that accepts a single argument. That argument's value should be the text entered in by the user. The method should return the translated text.
1. The team should create an extra JavaScript file that handles interacting with the form elements and determining which method should be called.

> **Optional Bonus 1**
>
> Find a way to write your IIFEs so that it doesn't matter whose module gets created first.

---

> **Optional Bonus 2**
>
> In addition to inserting the translated text into the HTML document, have the browser read the translated text to the user.
>
