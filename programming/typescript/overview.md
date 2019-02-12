= Typescript =
If you want type checking or high-quality code completion (also known as IntelliSense), you’ll want to use TypeScript, a superset of JavaScript (meaning every JavaScript file is also a TypeScript file… ostensibly).

TypeScript compiler is a node.js app.
TypeScript supports both ES7 features and JSX, and its output is ES5 or ES6 code.

npm install -g typescript
npm install -g typings

* npm i --save-dev typescript





var Id: number = 1;
var cost: number = 2.33;
var yes: boolean = true;
var arr: string[] = ["one", "two"];
var arr2: Array<number> = ["a", "b"];
var noVal = null;
Var anyType: any = "string";

--------------------------------------------------
function emptyFunc(p1: string, defaultArg = "val", optionalArg?: number): void {

}

--------------------------------------------------
Enum People {Brij, Vicky}
var x = People.Brij;
var y = People[0];

--------------------------------------------------
interface Person {
  hairColor: string;
  age: number;
  alive?: boolean;
  feed();
}
--------------------------------------------------
interface AddNums {
  (num1: number, num2: number)
}

var newNum: AddNums;

newNum = function(num1: number, num2: number) {

}

var z = newNum(4, 5);
--------------------------------------------------

interface Stringy {
  [index: number]: string;
}

var coolArray: Stringy;
coolArray = ["apple", "orange"];

--------------------------------------------------

class Person {
  name: string;
  age: number;
  hungry: boolean = true;

          constructor(name: string, age?: number) {
            this.name = name;
            this.age = age;
          }

          feed() {
            this.hungry = false;
            return "yummy!";
          }
}

var Brendan = new Person("Brendan", 21);
Brendan.feed();

--------------------------------------------------

class SecretAgent extends Person {

}
--------------------------------------------------

module Person {
  export interface PersonInterface {
    name: string;
  }
}


/// <reference path="Person.ts" />
module Person {
  export class Person implements PersonInterface {
    name: string;
  }
}

== npm scripts ==
"scripts": {
  "test": "echo \"Error: no tests installed\" && exit 1",
  "build": "tsc",
  "start": "node server.js"
},
The build script simply runs tsc which compiles your code according to the options in tsconfig.json. To invoke this script you write npm run build on the command line.

“But wait!” you may be thinking. “It’s really much easier to type tsc than npm run build!” That’s true, but there are two reasons to define a build script:
* If you installed TypeScript with --save-dev but not --global, you can’t run tsc directly from the command line because it’s not in the PATH.
* There’s a good chance your build process will become more complicated later. By creating a build script you can easily add other commands to the build process later.

Note: npm runs the prestart script automatically whenever someone runs the start script, so you could add this additional an additional script:

"prestart": "npm run build",
This would build your project whenever you start your server with npm start or npm run start.

== intellisense ==
To get IntelliSense for Node.js, you need to install type information for it with this command:

npm install @types/node --save-dev

= sources =
https://medium.freecodecamp.org/how-to-set-up-a-typescript-project-67b427114884
http://www.typescriptlang.org/play/
https://www.typescriptlang.org/docs/handbook/tsconfig-json.html
https://www.typescriptlang.org/docs/handbook/compiler-options.html
