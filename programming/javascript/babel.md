= babel =
* Transpiler
* Supports ES2015
* Supports all popular module formats
* Executed as a build step
* By default uses CommonJS
* pluggable architecture, you need additional packages to perform the transformation that you are interested in. Many transformations are grouped together in bundled presets


npm install babel-cli --save-dev
npm install babel-preset-es2015 --save-dev

$ ./node_modules/.bin/babel js --presets es2015 --out-dir build

= sources =
babeljs.io
