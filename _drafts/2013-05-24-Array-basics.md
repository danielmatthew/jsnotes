---
layout: post
title: Array Basics
---

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