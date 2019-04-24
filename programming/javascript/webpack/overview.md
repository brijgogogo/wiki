= webpack =
* bundles AMD, CommonJS, ES2015
* Code splitting: lets you to group your bundles so that you can optimize how to download your bundles
* Can bundle js files, images, css, other static assets
* you can preprocess (before bundling) your files by using loaders

npm install webpack --save-dev
./node_modules/.bin/webpack js/app.js build/bundle.js
<script src="/build/bundle.js" type="text/javascript"></script>


// support babel transpilation
npm install babel-loader babel-core

== configuration file ==
webpack.config.js


== sources ==
https://webpack.js.org/
webpack.github.io
