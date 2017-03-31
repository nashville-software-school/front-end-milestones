## Setup

### Create a new branch

`git checkout -b version09`

## Requirements

### Using Firebase references

In the [Firebase Setup](https://firebase.google.com/docs/web/setup#add_firebase_to_your_app) there are instructions on how to get CDN and app setup information for your Firebase app. After clicking 'Add Firebase to your web app' on your project's Firebase main page, copy the CDN link into your HTML, and copy the JavaScript snippet into your JavaScript to initialize your app.

```js
var config = {
  apiKey: "apiKey",
  authDomain: "projectId.firebaseapp.com",
  databaseURL: "https://databaseName.firebaseio.com"
};

firebase.initializeApp(config);
```

Then, in your JavaScript, you can create what's called a Firebase Reference.

```js
var myFirebaseRef = firebase.database().ref();
```

You will use this reference for authentication

### Authentication

For this exercise, you are going to force users to log in before they can use Music History.

> [Firebase docs](https://firebase.google.com/docs/auth/web/password-auth) for username and password authentication.

1. When the user first opens the application, there should be a username and password text field, a button labeled "Register", and a button labeled "Login".
1. If the user has filled in information in both text fields, and clicks the register button, you are going to [create an account in Firebase](https://firebase.google.com/docs/auth/web/password-auth#create_a_password-based_account) for that user.
1. If the user has filled in information in both text fields, and clicks the register button, you are going to [authenticate](https://firebase.google.com/docs/auth/web/password-auth#sign_in_a_user_with_an_email_address_and_password) that user.
1. In the navigation bar, add a "Log out" link or button.
1. When the user clicks on the logout element, you will [unauthenticate](https://firebase.google.com/docs/auth/web/password-auth#next_steps) the user.
1. When a user has been successfully authenticated, you can listen to that change of state with the [onAuthStateChanged](https://firebase.google.com/docs/auth/web/manage-users#get_the_currently_signed-in_user) method.
1. When you have authenticated a user, show the music filtering view.
1. When the user has been unauthenticated, show the login view again.
