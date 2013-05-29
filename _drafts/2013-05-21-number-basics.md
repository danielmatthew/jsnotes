---
layout: post
title: Number Basics
---

Declare variable as integer: var a = 123
Negative number: var b = -123
Can use decimal point too: var c = 1.5

No difference between number types.
In Javascript, operations will always return a floating-point number.
Need to watch out for rounding errors on occasions - solve by manually rounding, or represent numbers (money etc) using integers
Can represent large numbers using exponential representation. E.g, 1000000 becomes 1E6
Numbers beginning with a 0 are translated as octals. Javascript doesn't show error, but interprets back to decimal.
Can also use hexadecimal notation. Number begins with 0x - e.g. var hex = 0xf0