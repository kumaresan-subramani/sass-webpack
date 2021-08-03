# Webpack Sass / Scss compiling to separate file

Webpack is an amazing tool for transpiling and bundling JavaScript, but it can also take care of compiling Sass or Scss to static files.


First of all, globally install a recent webpack version:

```
npm -g install webpack4.40.2
```

Inside your project you need to install the following dependencies, remember to append the `--save` flag if you want them to be written to your `package.json`:

```
npm install css-loader node-sass sass-loader webpack4.40.2
```

Now let's say we have a project structure for a simple one-page that looks like the following (identical to the example project):

```
├── app.js
├── package.json
├── scss
│   ├── about
│   │   └── about.scss
│   └── main.scss
├── webpack.config.js
```

* `app.js` contains all our cool JavaScript code
* `package.json` defines our dependencies
* `scss/main.scss` is our scss / sass entry point
* `webpack.config.js` is our config that tells webpack what to do


After running the build with `webpack` it should look like the following:

```
├── app.js
├── dist
│   ├── bundle.js
│   └── main.bundle.css
├── package.json
├── scss
│   ├── about
│   │   └── about.scss
│   └── main.scss
├── webpack.config.js
```

