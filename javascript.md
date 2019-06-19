# javascript-cheatsheet
A cheatsheet with all essentials

## Comments
 Inline comments:
 ```
 // This is an in-line comment.
 ```

Multiline comments: 
```
/* This is a
multi-line comment */
````

## Variables
```
var name; // undefined
var name = "Anja"; // string literal
var number = 5; // integer
var boolean = true; // boolean
```
Use camelcase for the variable names.
```
var someRandomNumber = 19;
```

## Add, substract, multiply, divide
```
var add = 10 + 0; // returns 10
var substract = 10 - 2; // returns 8
var multiply = 12 * 2; // returns 24
var divide = 12 / 3; //returns 4
```

## Number increment and decrement
```
var i = 5; i++; // equals 'var i = i + 1;', returns i = 6;
var i = 5; i--; // equals 'var i = i - 1;', returns i = 4;
```

## Remainder operator
```
13 % 2 = 1 // 17 is odd)
52 % 2 = 0 // 52 is even)
```

## Compound assignment (addition, substraction, multiplication, division)
```
var 1 = 5; i += 6; // returns i = 11
var 1 = 5; i -= 1; // returns i = 4
var 1 = 5; i *= 2; // returns i = 10
var 1 = 5; i /= 2; // returns i = 2.5
```

## String literals
```
var name = "Anja" // string literal
```

Escaping strings with backslash
```
var string = "You are \"Amazing\", she said.";
var string = 'We\'re going to the park, want to come?'
```

Escape sequences:

|Code|Output|
|-|-|
|\'|single quote|
|\"|double quote|
|\\|backslash|
|\n|newline|
|\r|carriage return|
|\t|tab|
|\b|backspace|
|\f|form feed|

## Concatenate strings
```
var name = "human being"; var string = "Hi" + name + ", how are you?"
// returns "Hi human being, how are you?"

var string = "I am the first string. "; string += "I am the second string."
// returns "I am the first string. I am the second string.";
```

## String magic
Find the length
```
var string = "Hello";
string.length; // returns 5
```

Find the first character in a string 
```
var string = "Hello";
string[0]; // returns "H"
```

Find the last character in a string
```
var string = "Hello";
string[string.length - 1]; // returns "o"
```

## Arrays
```
var animals = ["cats", "dogs", "guinea pigs"]
```

Nesting Arrays
```
var multiArray = [["A", 1], ["B", 45], ["C", 67]]
```

Access array with index
```
animals[0]; // returns "cats"
multiArray[1]; // returns ["B", 45]
multiArray[1][0] // returns 45
```

Modify array data with index
```
var array = ["Hi", "Joe", "Bye"];
array[0] = "Ciao"; // array = ["Ciao", "Joe", "Bye"]
```

### push()
Add a value to the end of an array
```
var arr = [1,2,3]; arr.push(4); // returns [1,2,3,4]
```

### pop()
Remove a value at the end of the array
```
var arr = [1,2,3]; arr.pop(); // returns [1,2]
```

### shift()
Remove a value at the beginning of the array
```
var arr = [1,2,3]; arr.shift(); // returns [2,3]
```

### unshift()
Add a value to the beginning of an array
```
var arr = [1,2,3]; arr.unshift(4); // returns [4,1,2,3]
```

## Functions
Functions are reusable pieces of code.
```
function functionName() {
  return "I am a function!";
}

functionName(); // returns "I am a function"
```

You can pass parameters to the function.
```
function functionName(arg1, arg2) {
  return [arg1, arg2];
}

functionName("Joe", 14); // returns ["Joe", 14]
```

You can set a default value to a parameter.
```
function functionName(argument1 = "Hi", argument2 = 4) {
  return [arg1, arg2];
}

functionName(); // returns ["Hi", 4]
```

## If statement
```
var nr = 5;
if(nr === 5) {
  console.log("This number is a 5!");
} else if (nr > 5) {
  console.log("This number is higher than 5.");
} else {
  console.log("This number is lower than 5.");
}
```

## Switch statement
```
var  nr = 5;
switch(nr) {
  case 0:
  case 1:
  case 2:
    return "Low";
    break;
  case 3:
    return "Medium";
    break;
  case 4:
  case 5:
    return "High";
    break;
  default:
    return "Nothing matches in the switch: this is the default";
    break;
}
```

## Operators

### Equality operator '==' and '==='
Difference between the equality operator:
`==` can check the equality between two different `data types` and will convert them t0 be equal.
```
return 1 == "2"; // returns false
return 1 == "1"; // returns true
```

`===` is a strict equality, meaning it does not perform a type conversion. If the `data types` are not the same, this equation will return false.
```
return 1 === 1; // returns true
return "Hi" === "Hi"; // returns true
return 1 === "Hi"; // returns false
```

### Inequality operator '!=' and '!=='
```
return 1 != "2"; // returns true
return 1 != "1"; // returns false

return 1 !== 1; // returns false
return "Hi" !== "Hi"; // returns false
return 1 !== "Hi"; // returns true
```

### Greater than & greater than or equal to operator
```
return 1 > 0; // returns true
return 4 > 10; // returns false
reutrn 4 >= 4; // returns true
```

### Less than & less than or equal to operator
```
return 1 < 0; // returns false
return 1 < 4; // returns true
return 4 <= 5; // returns true
```

### AND operator
```
var nr = 5;
if(nr > 0 && nr < 10) {
  return "Number is between 0 and 10";
}
```

### OR operator
```
var nr = 5;
if(nr > 0 || nr === 5) {
  return "Number is bigger than 0 or number is a 5";
}
```

## Conditional Ternary operator
The Ternary operator is a shorter version of the `if else` statements: `condition ? statement-if-true : statement-if-false`.
```
// this...
var string = "Hello";
var a = "I'm true";
var b = "I'm false";

if(string === "Hello") {
 return a;
} else {
 return b;
};

//...becomes this:
return string === "Hello" ? a : b; // returns a
```
You can use all operators in the condition:
```
var number = 12;
return number > 10 ? a : b; // returns a

var boolean = false;
return boolean ? a : b; // returns b
```
You can also chain these operators, although it does not always benefits the readability of your code:
```
var bool = false;
var str = "Hi";
var a = 1;
var b = 2;
var c = 3;

return bool ? a : str === "Hi" ? b : c; // returns b
```

## Objects
```
var objectName = {
  "name": "Nugget",
  "tail": 1,
  "legs": 4,
  "toys": ["bouncing ball", "mouse"]
}
```
Accessing object properties:
```
objectName.name; // returns "Nugget" // using dot notation
objectName["name"]; // returns "Nugget"// using bracket notation
```
Updating object properties:
```
objectName.name = "Butters";
```
Add new property to object:
```
objectName.sound = "miauw"; // using dot notation
objectName["sound"] = "miauw"; // using bracket notation
```
Delete property from object:
```
delete objectName.sound; // using dot notation
delete objectName["sound"]; // using bracket notation
```
Testing objects for property: check if a property excists in the object:
```
objectName.hasOwnProperty("name"); // returns properties value
objectName.hasOwnProperty("favorite spots"); // returns "Not Found"
```
## Iterations
### while & do ... while loop
```
var array = [];
var i = 0;
while(i < 10) {
  array.push(i);
  i++;
}
// returns array = [0,1,2,3,4,5,6,7,8,9]
```

Do ... while loop: this loop will always execute the code in `do`, even if the condition in the `while` loop is not met.
```
var array = [];
var i = 0;
do {
  array.push(i);
  i++;
} while (i < 5);
```

### for loop
A for loop gets three statements: `for ([initialization]; [condition]; [final-expression])`.

The `Initialization` statement executes one time before the loop starts.

The `condition` statement is the condition that has to return true in order to keep looping. When this statement returns false, the for loop stops.

The `final-expression` statement exectures every time a loop ends.
```
var array = [];
for (var i = 0; i < 10; i++) {
  array.push(i);
}
// returns array = [0,1,2,3,4,5,6,7,8,9]
```
Backwards iteration:
```
var array = [];
for (var i = 5; i > 0; i--) {
  array.push(i);
}
// returns array = [5,4,3,2,1]
```
Odd numbers iteration:
```
var array = [];
for (var i = 0; i < 10; i += 2) {
 array.push(i);
}
// returns array = [1,3,5,7,9]
```
Iterate through array:
```
var array = [1,2,3,4,5];
for (var i = 0; i < array.length; i++) {
 console.log(array[i]);
}
```
Nesting for loops:
```
var array = [1,2], [3,4], [5,6];
for (var i = 0; i < array.length; i++) {
 for (var k = 0; k < array[i].length; k++) {
  console.log(arr[i][k]);
 }
}
```

## Fractions and whole numbers
### Random fraction
```
Math.random(); // returns a fraction between 0 and 1. Can be 0 but never 1
```
### Random whole number
Because the fraction can't return a 1: if you want to have a random whole number returned, you'll need to multiply the result and round off the decimal with the `Math.floor()` function.
```
Math.floor(Math.random() * 20); // returns a random number between 0 and 19
Math.floor(Math.random() * 10); // returns a random number between 0 and 9
```
### Random number within range
```
Math.floor(Math.random() * (max - min + 1)) + min; // returns a random number between min and max value
```
## ParseInt() function
This function parses a string and returns an integer.
If the first character in the string can't be converted, the function returns `NaN`.
```
var strToInt = parseInt("007"); // returns 7
```
The function takes another argument: redix. This specifies the base of the number in the string (between 2 and 36). See the MD docuimentation to learn more about `redix`.
```
var strToInt = parseInt("10011", 2); // returns 19
```
