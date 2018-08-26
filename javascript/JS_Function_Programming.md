* Immutability
Object.assign({}, obj, {x:obj.x + 1})

const incrementObject = obj =>
  ({...obj, x: obj.x + 1})

use Array.concat instead of Array.push
or
[...prevArray, newItem]


* Pure Function
do not cause side effects

* Higher Order function

* Currying

* Recursion

* Composition
chaining, compose function, 
