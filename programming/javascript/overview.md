= javascript =
- Released in 1995
- European Computer Manufacturers Association (ECMA) in in charge of changes.
- ES5 in 2009
- ES2015 onwards yearly releases.
- ESNext : Anything that’s part of the stage proposals
  - Stage 0: newest proposals
  - Stage 1
  - Stage 2
  - Stage 3
  - Stage 4: finished proposals

Browser Compatibility with JS: http://kangax.github.io/compat-table/esnext/


* [[variables]]
* [[JS_string]]
* [[functions]]
* [[JS_Object]]
* [[JS_Arrays]]
* [[classes]]

* [[js_compilation]]
* [[modules]]

* [[JS_Function_Programming]]
* [[decorator]]
* [[transpilers]]
* [[singleton]]
* [[prototype]]
* [[polyfills]]
* obj?.propName : safe navigation operator


* [[async_js]] promises, observables, fetch

* [[../nodejs/overview|nodejs]]
* [[expressjs]]

https://www.prisma.io/

* [[js_app_questions]]



== flavors of javascript ==
* [[ecmascript/overview|ecmascript]]
* [[../typescript/overview|typescript]]
* flow

== frontend frameworks ==
* [[../reactjs/overview|react]]
* [[../angular/overview|angular]]
* vue.js
* [[../d3/overview|d3]]
* mithril
* jQuery
* [[web_assembly]]
* preact
* [[svelte]]

== package managers ==
* [[../nodejs/yarn|yarn]]
* [[../nodejs/npm|npm]]  (npx)

== useful packages ==
- npm-check
- yo

# package.json
- project metadata (name, authors, license)
- describes projects
- lists dependencies

# package-lock.json
- records the exact versions that were installed
- Package.json can be loose in its specification of dependency version (^, ~)
- recommended to check this file into source control
- helpful if you need to re-create the exact dependency versions in your project

# package version
Version numbers in npm are parsed by a component called semver.
major.minor.patch
version modifiers: ~, ^
package >= 1.2.7 : install any pckage greater than 1.2.7
package ~1.2.3 : install patch level changes (1.2.3, 1.2.4, but not 1.3.x nor 2.x)
package ^1.2.3 : insdtall minor updates (1.2.3, 1.2.4, 1.5.6, but not 2.x)
@ indicates version tag
package@2.0.0 : exact package version
package@latest : latest stable version
package@next : latest beta version
https://blog.fullstacktraining.com/what-is-semantic-versioning/



= minifiers, obfuscators =
* UglifyJS
* JSMin
* Closure [[Compiler]]

== testing libraries ==
# unit tests
- [[Jest]]
- Jasmine
- Mocha
- Ava
- Tape
# Integration tests
 - [[Puppeteer]]: integration tests

== Continuous Integration (CI) ==
- Travis CI
- Circle CI



== desktop frameworks ==
* electron
* react native

== build & packaging tools ==
* [[webpack/overview|webpack]]
* grunt
* browserify
* gulp
* parcel

== other libraries ==
* lodash
* ramda
* underscore
* graphql
* [[rxjs/overview|rxjs]]

== linting utilities ==
Linter - checks syntax, finds problems, could also enforce code styles
* JSLint - original JavaScript linter by Douglas Crockfords
* JSHint - in 2011, by Anton Kovalyov
* [[ESLint]] - by Nicholas Zakas (most popular)

= formatting utilities =
- Prettier

== templating libraries ==
* jade
* pug
* mustache
* handlebars



== reading list ==
https://github.com/AlexanderEllis/js-reading-list
https://stateofjs.com/
https://2018.stateofjs.com/
https://npm-stat.com/
https://ashleynolan.co.uk/blog/frontend-tooling-survey-2018-results
https://blog.logrocket.com/discussing-the-over-engineering-trap-in-typescript/
