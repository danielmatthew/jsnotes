---
layout: post
title: Number Functions
---

Can extract numbers from strings:
Use native function parseInt() or parseFloat()
Can specify the base as a second parameter: parseInt("019", 10).   Best practice to include radix by default.
parseInt can grab number from string if first
NaN - Not a Number. Before operations, should attempt to check for presence of NaN. Can use strict equality operator to test,
but NaN has curious property of not actually being equal to itself.
Use isNaN() to test instead.
parseFloat() has similar caveats to parseInt()

In-built functions organised under Math object:

Math.random() - default bounds between 0 and 1
Math.round - to nearest whole number
Math.floor - rounds down - use to create integer from floating point number.
Math.ceil - always rounds up
Math.pow(base, exponent)
Math.sqrt()