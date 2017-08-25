###npm: Node Package Manager

A package manager automates the process of installing computer programs used in applications including bootstrap, grunt, and jquery to name a few. See [wikipedia](https://en.wikipedia.org/wiki/Package_manager) for more information on package managers.

When installing dependencies on an existing project (cloned or forked from GitHub) [npm](https://www.npmjs.com/) requires the command `npm install` in the terminal to install dependencies included in the `package.json`. To start a new project, the command `npm init` will create a that json file along with `install --save-dev` to install dev dependencies used in development, and/or `--save` to install dependencies needed for the application to run.

`npm` was initially created to install backend, or server-side, dpenedencies. But as it becomes more and more robust, front-end dependencies can also be installed using npm. Many professional development shops use npm in conjunction with a tool like [Browserify](http://browserify.org/) which will [transpile](https://en.wikipedia.org/wiki/Source-to-source_compiler) a Node.js module for use in the browser.

--

#### The typical commands 
* `npm init`
* `npm install <package_name> --save-dev`
* `npm install <package_name> --save`
* package.json

