
# React.js

You're going to be following along with the standard [React tutorial](https://facebook.github.io/react/docs/tutorial.html) with just minor modifications.

## Setup
```bash
cd lib
npm install -g babel-cli
npm install babel-preset-react
bower install babel react

```

## Hello, world

Add the following code to your body.

```html
  <div id="example"></div>


  <script src="lib/bower_components/babel/browser.min.js"></script>
  <script src="lib/bower_components/react/react.min.js"></script>
  <script src="lib/bower_components/react/react-dom.min.js"></script>

  <script type="text/babel" src="app/hello.js"></script>
```

Now create the `app/hello.js` file and add the following to it.

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```

Now load your browser and you should see "Hello, world!"

## Using Babel

Babel is a popular library which allows JavaScript developers to write ES6 compliant syntax, and have it compiled down to ES5 for cross-browser compatibility.

You're going to update Grunt to compile the React component, written in JSX syntax, before the JSHint task kicks off. Otherwise, it will yell at you because JSX components are not valid JavaScript.

```js
module.exports = function(grunt) {

  grunt.initConfig({
    babel: {
        options: {
            sourceMap: true,
            presets: ['./node_modules/babel-preset-react']
        },
        dist: {
            files: {
                '../build/hello.js': '../app/hello.js'
            }
        }
    },
    jshint: {
      files: ['../build/**/*.js']
    },
    sass: {
      dist: {
        files: {
          '../styles/main.css': '../sass/main.scss'
        }
      }
    },
    watch: {
      javascripts: {
        files: ['../build/**/*.js'],
        tasks: ['jshint']
      },
      babelify: {
        files: ['../app/**/*.js'],
        tasks: ['babel']
      },
      sassy: {
        files: ['../sass/**/*.scss'],
        tasks: ['sass']
      }
    }
  });

  require('matchdep').filterDev('grunt-*').forEach(grunt.loadNpmTasks);
  grunt.registerTask('default', ['babel', 'jshint', 'sass', 'watch']);
};
```

```bash
# Watch task for compiling JSX components
babel --presets ./lib/node_modules/babel-preset-react app --watch --out-dir build
```