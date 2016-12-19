
# Steps for New Project Setup

```
    mkdir newProject
    cd newProject
```

### If using any bower components (e.g. jquery & bootstrap):
```
    bower init    (answer several questions)
    bower install jquery --save (or --save-dev?)*
    bower install bootstrap --save (or --save-dev?)*

    * --save: This is used to save the package required for the application to run.
    * --save-dev: This is used to save the package for development purpose. Example: unit tests, minification.
```

### If using any npm components (grunt/jshint/watch):\
```
    npm init    (answer several questions)
    npm install grunt --save-dev
    npm install jshint --save-dev
    npm install grunt-contrib-jshint --save-dev
    npm install jshint-stylish --save-dev
    npm install grunt-contrib-watch --save-dev
```
---
### Git setup:
#### Create repo on github.com and copy remote url. Then use that url in the commands below
```
    git init
    git remote add origin http://<githubURL>
    touch .gitignore
    touch README.md
```

#### Add to README.md
```
    What your program does
    How to pull it down from github and run it
```
##### Or at the very least:
```
    The name of the app
```

##### IMPORTANT: Add and commit the README before switching to a new branch to begin creating other files
```
git add README.md
git commit -m "Add README"
git push -u origin master
```
##### This will assure that the master branch doesn't "disappear" when you switch to your new branch
##### Now switch to a new branch. _Never work on `master`_
```
git checkout -b <my-branch>
```
---

### Standard files/dirs:
```
    touch index.html
    mkdir styles
    mkdir scripts
    touch js & css files
    touch Gruntfile.js
    touch .jshintrc (note the ".")
```

### Add to .gitignore:
```
    .DS_Store
    bower_components
    node_modules
```

### Add to Gruntfile.js:
```
    Example code in Notes
    Change files watched in 2 places to "scripts/*.js"
```

### At the top of all js files:
```
    "use strict";
```

### Add the basics to .jshintrc:
```
{
  "predef": [ "document", "jQuery", "$", "console" ],
  "esversion": 6,
  "globalstrict": true
}
```

### Open your Gruntfile.js and paste in the following code:
```
module.exports = function(grunt) {

  grunt.initConfig({
    jshint: {
      files: ['./javascripts/**/*.js']
    },
    watch: {
      javascripts: {
        files: ['./javascripts/**/*.js'],
        tasks: ['jshint']
      }
    }
  });

  require('matchdep').filterDev('grunt-*').forEach(grunt.loadNpmTasks);
  grunt.registerTask('default', ['jshint', 'watch']);
};
```

### In another Terminal tab run Grunt to run your registered default tasks:
```
    grunt
```

### On the command line
```
    http-server
```
