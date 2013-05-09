# Javascript Notes

## Strings
String methods include
* indexOf: discover the character at the specified number
* substr: grab a subset of the characters contained within a string

Strings are immutable - they cannot be changed once defined. But can make a new string by concatenating several together.

## Numbers
Declare variable as integer: var a = 123
Negative number: var b = -123
Can use decimal point too: var c = 1.5

No difference between number types. 
In Javascript, operations will always return a floating-point number.
Need to watch out for rounding errors on occasions - solve by manually rounding, or represent numbers (money etc) using integers
Can represent large numbers using exponential representation. E.g, 1000000 becomes 1E6
Numbers beginning with a 0 are translated as octals. Javascript doesn't show error, but interprets back to decimal.
Can also use hexadecimal notation. Number begins with 0x - e.g. var hex = 0xf0

Can extract numbers from strings: 
Use native function parseInt() or parseFloat()
Can specify the base as a second parameter: parseInt("019", 10).   Best practice to include radix by default.
parseInt can grab number from string if first 
NaN - Not a Number. Before operations, should attempt to check for presence of NaN. Can use strict equality operator to test,
but NaN has curious property of not actually being equal to itself.
Use isNaN() to test instead.
parseFloat() has similar caveats to parseInt()

Operators include:
+, -, *, and /
Division in Javascript can return floating point numbers
Modulo - %: returns remained after division of two operands. 15 % 10 = 5
Operands wrapped in parentheses always evaluated first.

Numbers can be compared using: 
<, >, <=, >=, === (equality), !==

In-built functions organised under Math object:

Math.random() - default bounds between 0 and 1
Math.round - to nearest whole number
Math.floor - rounds down - use to create integer from floating point number.
Math.ceil - always rounds up
Math.pow(base, exponent)
Math.sqrt() 

## Arrays
Arrays represent list of objects
Basic syntax: var x = ["variable", "variable", "variable"];
Can obtain size of array through .length property
Can store functions within an array!
Array within array counts as one element within original array
Create empty array: var array = [];
or var array = new Array(); - use this syntax when wanting to predefine the size of the array. Could be useful when wanting to keep tabs on memory.

Getting and setting array values
var word = my_array[0] - right hand side of assignment means get
myArray[0] = "lol" - LHS is set
Can run functions from within array:
var my_array[, , function(a) {return a * 2;}]
var doubler = my_array[3];

### Array Methods
Push and Pop
toString() - takes representation of array and turns it into string
push() - adds specified element to end of array
pop() - no arguments; returns last value of array

unshift(val) - analogous to push, but works on start of array
shift() - pop, but works on start of array

sort - default sort as strings. Can pass comparator function to sort as though they were numbers:
    my_array.sort(function (a,b) { return a - b;});
Can also randomly sort array like so:
    my_array.sort(function (a,b) { return Math.random() - 0.5;});

.reverse - flips array 
.concat - appends all values of one array to another. eg. z = x.concat(y);
.slice(start, end) - creates new array containing values from start index to end index. 
.join(separator) - 'joins' contents of array with specified separator. Could be used to create URL slug? 


## Callbacks
Helps prevent client being frozen as we wait for sequence of functions to run.
Better to make asynchronous request and provide callback function which is invoked on return.




