# Angular 103

## Handling authentication in Angular/Firebase application

The `onAuthStateChanged` listener will be very helpful when dealing with authentication. You can utilize the `run()` method on a module, which executes every time the page is loaded, or a view is switched.

```js
var songApplication = angular.module("SongApp", []);

app.config(['$routeProvider',
  function($routeProvider) {
    $routeProvider.
      when('/start', {
        templateUrl: 'partials/song-list.html',
        controller: 'SongCtrl'
      }).
      when('/login', {
        templateUrl: 'partials/authenticate.html',
        controller: 'AuthCtrl'
      });
  }
]);

songApplication.run(["$location", function ($location) {
  firebase.initializeApp({
    apiKey: "apiKey",
    authDomain: "projectId.firebaseapp.com",
    databaseURL: "https://databaseName.firebaseio.com"
  });

  var firebaseBaseRef = firebase.database().ref();

  firebaseBaseRef.auth().onAuthStateChanged(function (user) {
    if (user) {
      $location.url("/start");
    } else {
      $location.url("/login");
    }
  });
}]);
```


