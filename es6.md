# ECMAScript 6 (ES6)

## `var` versus `let`
A var can be redefined after it is declared. A let can not be redefined after it is declared. This helps you protect those variables you don't want to excidentally override in other pieces of code.
```
var dog = "Max";
var dog = "Fluffy";
console.log(dog); // returns "Fluffy"

let dog = "Max";
let dog = "Fluffy"; // throws an error: variable already declared
dog = "Fluffy"; // let variable is changeable
console.log(dog); // returns "Fluffy"
```
## Read only variable Constant
If you have a variable with a constant value, that will not change, you can declare it as a `constant`. 
This constant will be read-only. 
```
"use strict"
const FOOD = "Panecakes";
FOOD = "Yoghurt"; // throws an error
```
Notice: objects, arrays and functions declared with `const` are still mutable.
```
const array = [1,2,3];
array[1] = 4;
console.log(array); // returns [1,4,3]
```
### PreventObject mutation
You can declare that an object may not be mutated, by calling the `freeze` function.
```
let OBJECT = {
  "name" : "Nugget",
  "legs":4,
  "tail":1,
  "toys":["ball","sister"]
}
Object.freeze(OBJECT);
OBJECT.name = "Butters"; // will be ignored, but does not throw an error
```
## Aonymous arrow functions
Functions that are not named, and can be written inline.
```
// old notation
const functVar = function() {
  const var = "value";
  return var;
}
// ES6 notation
const functVar = () => {
  const var = "value";
  return var;
}
// Inline ES6 notation
const functVar = () => "value"

// Inline ES6 notation with function parameters
const functVar = (value) => value * 2;
```
