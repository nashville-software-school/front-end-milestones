## Setup

### Create Exercise Directory

```bash
mkdir -p ~/workspace/exercises/rich-browser/family && cd $_
```

## Requirements

1. Create a new Firebase application. Go to your dashboard and fill out the form. Application name should be "family", and provide a unique URL. (e.g. `nss-steve-family`)
1. Using Browserify, build a modular application that:
    1. Reads all family members from your Firebase DB and lists them in the browser.
    1. Lets you add new family members.
    1. Lets you delete family members (like that annoying nephew you can't stand).
1. At the minimum, you should create the following modules:
    1. Main module
    1. Module that handles adding family members to Firebase
    1. Module that handles deleting family members from Firebase.
    1. Module that handles listing family members.
1. Use the JSON structure shown below when adding a family member.  For the skills array, have a `<textarea>` field in your form where the user can enter in a comma-delimited list of skills that you will convert into an array.
1. Use XHR calls to handle all operations with Firebase.

> **Family member JSON stucture**
>
> ```
> {
>   "family": [
>     {
>       "name": "First Last",
>       "age": 4,
>       "gender": "male",
>       "skills": [
>         "burping",
>         "farting",
>         "inappropriate shouting",
>         "tantrums"
>       ]
>     }
>   ]
> }
> ```
> 