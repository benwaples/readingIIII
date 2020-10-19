# Reading Summary for Class 26

## [intro into webpack](https://www.freecodecamp.org/news/an-intro-to-webpack-what-it-is-and-how-to-use-it-8304ecdc3c60/)

webpacks were introduced because the application package had gotten to be so big that it became clunky and the developer code was very different from the browser readable code. 

> Webpack is a static module bundler

Webpack goes through the package and creates a dependency graph, containing all modules which the app requires to function normally. Then based on the graph, webpack creates a new package consisting of only the files needed to compile.

## [Webpack Concepts](https://webpack.js.org/concepts/)
### Core concepts: 
* entry
* output
* loaders
* plugins
* mode
* browser compatibility

### entry: 
```js
module.exports = {
  entry: './path/to/my/entry/file.js'
};
```
### Output
```js
const path = require('path');

module.exports = {
  entry: './path/to/my/entry/file.js',
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'my-first-webpack.bundle.js'
  }
};
```
### Loaders
Loaders help webpack process other types of files and convert them into valid modules. i.e. css to js
```js
const path = require('path');

module.exports = {
  output: {
    filename: 'my-first-webpack.bundle.js'
  },
  module: {
    rules: [
      { test: /\.txt$/, use: 'raw-loader' }
    ]
  }
};
```
### Plugins
help with bundle optimization, asset managment, and injection of env variables.
```js
const HtmlWebpackPlugin = require('html-webpack-plugin'); //installed via npm
const webpack = require('webpack'); //to access built-in plugins

module.exports = {
  module: {
    rules: [
      { test: /\.txt$/, use: 'raw-loader' }
    ]
  },
  plugins: [
    new HtmlWebpackPlugin({template: './src/index.html'})
  ]
};
```
### Mode
enable webpack to optimize for each environment (dev/ production/ none)
```js
module.exports = {
  mode: 'production'
};
```
### Browser Capability
Webpack help with making code compatible with more browsers, and browser versions

## [Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
Webpack makes JSX into js

## [React Hello World](https://reactjs.org/docs/hello-world.html)

## [JSX intro](https://reactjs.org/docs/introducing-jsx.html)