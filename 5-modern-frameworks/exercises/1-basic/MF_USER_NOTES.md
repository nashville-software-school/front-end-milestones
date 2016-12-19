# User Notes with Authentication

In this exercise, you'll be requiring users to register and log into your application before they can use it. The user interface is very simple once they log in, because this is a basic application that will allow them to enter notes, and then view all notes.

## Setup

```
mkdir -p ~/workspace/exercises/modern-framework/user-notes && cd $_
```

## Requirements

### Firebase

1. Create a Firebase collection named `notes`
1. Use the basic Firebase email/password authentication to register users for your application.

### Application

1. Create an Angular application module.
1. Create 4 partials for views.
    1. A registration view
    1. A login view
    1. A new note form
    1. A note list form
1. Configure your application to support the following routes.
    1. `/register`
    1. `/login`
    1. `/notes`
    1. `/new`
1. Write a controller for each of the partials

### New Note Form

Display a text field labeled `Enter note:` and a button labeled `Save`. When the button is clicked, save a new item in the Firebase `notes` collection, along with the current user's unique id.

### Note List

When the user visits the `/notes` URL, the user should see all of the notes that were entered by that user, and no others. Use the `orderBy` and `equalTo` parameters in the `$http` request to only return notes created by the current user.






