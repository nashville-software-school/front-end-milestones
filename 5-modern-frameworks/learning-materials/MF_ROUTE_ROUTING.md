# Route Routing

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```
mkdir -p ~/workspace/exercises/modern-framework/route-routing && cd $_
```

## Requirements

For this exercise, you're going to create a basic application, with a two views. Each view will provide information about a famous American highway. Each will have a title show the name of the highway, and an element in which the description of the highway will be displayed.

You will need:

1. An Angular application module. Inject `ngRoute` into your applcation.
1. A `config` section for your application where you set up two routes.
    1. Famous highway #1
    2. Famous highway #2
1. Two controllers defined in your application.
1. Two partials - one bound to one of the controllers.
1. Each controller will have two scope variables.
    1. `$scope.highwayName`
    1. `$scope.highwayDescription`
1. You provide the name and description for each highway that you find via research.

Start `http-server` and access both of the routes and verify that each highway's information displays correctly.

> Example routes: 
> 
>   http://localhost:8080/#/blueridgeparkway
>   
>   http://localhost:8080/#/route66

