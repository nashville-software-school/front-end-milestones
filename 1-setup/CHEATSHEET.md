# Steps for New Project Setup

```
mkdir newProject
cd newProject
```

## Installing npm components

```
npm init    (answer several questions)
npm install grunt --save-dev
npm install jshint --save-dev
npm install grunt-contrib-jshint --save-dev
npm install jshint-stylish --save-dev
npm install grunt-contrib-watch --save-dev
```

## Git Setup

First, create a new repository on Github, and copy the SSH URL for connecting.

```
git init
git remote add origin http://<githubURL>
touch .gitignore
touch README.md
```

### Minimum contents of .gitignore:

```
.DS_Store
bower_components
node_modules
```

### What to put in the README

1. What your program does
1. What, if any, prerequisite software needs to be installed before running your code
1. Steps the user needs to follow to run the code
1. A description of the main features

> **IMPORTANT:** `git add` and `git commit` the README before switching to a new branch to begin creating other files

```
git add README.md
git commit -m "Add README"
git push -u origin master
```

### Branches

Always do your work on a branch. **Never work on the master branch**.

```
git checkout -b <descsriptive-branch-name>
```

## Standard files and directories

```
touch index.html
mkdir styles
mkdir scripts
touch js & css files
touch Gruntfile.js
touch .jshintrc (note the ".")
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

### Sample Gruntfile.js

Open your Gruntfile.js and paste in the following code:

```js
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

## Starting the processes

Open a terminal session and run Grunt to execute the defined tasks.

```
grunt
```

Open another terminal session and start your file server.

```
http-server
```
