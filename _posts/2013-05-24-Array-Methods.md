---
layout: post
title: Array Methods
---

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

Array Splicing
Keyword available: 'delete' - clumsy
my_array.splice(index, number of elements to remove);
Can also use splice to insert elements: my_array.splice(2, 0, 'two'). Each extra parameter becomes a new element to be added to the array.
