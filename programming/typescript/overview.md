= Typescript =

npm install -g typescript
npm install -g typings






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

