# Solar System Info with Browserify

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.

```bash
mkdir -p ~/workspace/exercises/mjd/solar-system && cd $_
```

1. Use `npm` to install Browserify, and any other packages you need to compile your modules.
2. Make sure you have the Grunt task running that will build the distribution bundle file.

## Instructions

You'll be creating a web page that will display important scientific data about all eight planets in our solar system. The information about each planet will be separate modules.

1. Each module will export a single function named `outputTo` that will accept a single argument. That argument's value will be the DOM element reference into which it will insert information about a planet.

    ```js
    function outputTo(domElement) {
      domElement.append(...);
    }
    ```
    
2. Each module should output the following information.
    1. Name
    2. Year discovered
    3. Mass
    4. Size
    5. Distance from Sun
    6. Atmosphere composition
    7. Satellites
    8. Name of any probes/orbiters/explorers that have visited or landed on that planet
3. Create a main module that uses `require` to include each planet's module as a dependency and then subsequently calls the `outputTo()` method for each one, in the right order.

## Bonus stretch goal

Once you've got the basic implementation working, find a way to have the `outputTo()` only defined once, and still be able to output each planet's information to the DOM. It can't be defined in the **main** module.


