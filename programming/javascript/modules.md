= modules =
A JavaScript module is a piece of reusable code that can easily be incorporated into other JavaScript files without causing variable collisions. JavaScript modules are stored in separate files, one file per module.


* [[IIFE]]
* [[Revealing_Module_Pattern]]

== Module formats ==
Syntax used to define a module

Non-native formats (support not built into Javascript language):
- [[AMD]] : Asynchronous Module Definition
- [[CommonJS]]
- [[UMD]]
- [[System.register]]

Native format:
- [[ES2015]] (ES6 Modules)


== Module loaders ==
Javascript libraries that understand module formats, how to load them and how to execute them.

- [[RequireJS]]
- [[SystemJS]]

== Module Bundlers ==
Module bundlers solve the same problem as "module loaders", but they do it at build time.
Combine modules into fewer files.
May decrease application startup time
Bundling step may also involve transpiling.

workflow:
AMD/CommmonJS/ES2015 --> Bundler --> bundle.js --> browser

- [[browserify/overview|browserify]]
- [[webpack/overview|webpack]]



== sources ==
https://www.jvandemo.com/a-10-minute-primer-to-javascript-modules-module-formats-module-loaders-and-module-bundlers/
http://www.commonjs.org/specs/modules/1.0/
https://github.com/amdjs/amdjs-api/blob/master/AMD.md
https://github.com/systemjs/systemjs
https://stackoverflow.com/questions/40669906/what-is-the-need-for-systemjs-in-angular2/40670147#40670147
https://addyosmani.com/resources/essentialjsdesignpatterns/book/

