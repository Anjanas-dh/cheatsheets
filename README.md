# javascript-cheatsheet
A cheatsheet with all essentials, including ES6

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

## number increment and decrement
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

## Objects
```
var object = {
  "name": "Nugget",
  "tail": 1,
  "legs": 4,
  "toys": ["bouncing ball", "mouse"]
}
```
Accessing object properties:
```
object.name; // returns "Nugget" // using dot notation
object["name"]; // returns "Nugget"// using brackets notation
```
Updating object properties:
```
object.name = "Butters";
```
Add new property to object:
```
object.sound = "miauw"; // using dot notation
object["sound"] = "miauw"; // using brackets notation
```
