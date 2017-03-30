# National Park Service

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```
mkdir -p ~/workspace/exercises/modern-framework/national-parks && cd $_
```

> :pencil2: Ensure you have Angular, ng-route, and the Firebase libraries installed and linked in your HTML file.

## Requirements

For this project, you must use Angular controllers, Angular factories and Firebase storage and Firebase authentication. You will be creating an  application that lets users keep track of National Parks that they would like to visit.

![bitterroot](http://wac.450f.edgecastcdn.net/80450F/klyq.com/files/2011/07/paradisesign-300x225.jpg)
<img src="http://www.forestcamping.com/dow/graphics/nant.jpg" height="225">

### Firebase

1. Create a Firebase collection named `forests`
1. Create a Firebase collection named `visitors`
1. Create a Firebase collection named `visitor_favorites`
1. Use the basic Firebase email/password authentication to register users for your application.

You determine the structure of each object in the `forests` collection. At the very minimum, it should have a `name` and `description` property. Use the Firebase console, Postman, CURL, or whatever method you like to get data inserted for each of the collection.

The `visitors` collection is for storing information about the users that register for your application. When a user registers, their unique id should be stored in the `visitors` collection.

The structure of the `visitor_favorites` collection should be as follows.

```js
"{firebase_unique_identifier}" :{
    "forest": "{the unique identifier of a forest",
    "visitor": "{the unique identifier of a visitor"
}
```

### Application

1. Create an Angular application module.
1. Create 4 partials for views.
    1. A registration view
    1. A login view
    1. A forest listing view
    1. A forest detail view
1. Configure your application to support the following routes.
    1. `/register`
    1. `/login`
    1. `/forests`
    1. `/forests/favorite`
    1. `/forest/:id`
1. Write a controller for each of the partials
1. Write a factory for getting forest related information that the controller for the list view, and the detail view, can both use. It should return an object with at least two functions on it - `getForests()` and `getForest(id)`. There may be more functions needed. Remember to use the `orderBy` and `equalTo` parameters on the request to get single forest.
1. Write a factory that handles all authentication methods for your application. Both the registration controller and the logic controller should use it.

### Forest Details

Display the name and description of the forest - and any other details you are storing - as well as an affordance for the user to favorite the forest, indicating that it will be visited in the future.

### Favorites

When the user visits the `/forests/favorite` URL, the user should see all of the forests that were favorited. There should be a function returned from the forest factory that queries the `visitor_favorites` collection, and uses the `orderBy` and `equalTo` parameters to only return items created by the current user.
