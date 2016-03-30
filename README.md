#Webpack as your module bundler

##Why use a module bundler?
With modular programming becoming the industry standard, developers are using module bundlers like Browserify or Webpack to organize code structures and reuse modules/components among multiple entry points.

##So Why WebPack?
1. Great for single page application
2. It manages modules and their dependencies and transforms static assets to build bundles
3. Webpack Developer Server allows for React Hot-Reload.

##Using WebPack
```npm install -g webpack```

Webpack is a command line tool that runs globally, kind of like how you run gulp.
```$ webpack ./entry.js bundle.js```
This will compile your entry.js into a bundle.js file.

Running webpack in the command line by itself, it will run the webpack.config.js that comes standard with webpack.
```
module.exports = {
    context: __dirname + "/app",
    entry: "./entry.js",
    output: {
        path: __dirname + "/dist",
        filename: "bundle.js"
    }
}
```
##Webpack Developer Server
```npm install -S webpack-dev-server```
Webpack Developer Server tracks changes inside your javascript file.
```
"devDependencies": {},
"scripts": {
  "dev": "webpack-dev-server --content-base src --inline --hot",
  "test": "jasmine-node spec --verbose"
},
```
After you have your script alias, run ```npm run dev``` to start webpack server and watch for changes

##External Resources
[LearnCode.Academy](https://www.youtube.com/watch?v=9kJVYpOqcVU)

[^^Github Repo](https://gist.github.com/learncodeacademy/25092d8f1daf5e4a6fd3)

[Webpack Docs](https://webpack.github.io/docs/)
