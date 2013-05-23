---
layout: post
title: Function declarations versus function expressions
---
## Function declaration
A function declaration is written like so:
    function example() {}

A declared function is evaluated at parse-time - when the browser's Javascript engine gives it the once-over to see what it contains - and thus are loaded before any code is executed.
In practical terms, this function can now be called at anytime: perhaps in code that is defined before the function. This is due to the idea of hoisting: a facet of the language that allows variables to be 'hoisted' to the top of the current scope.  The same principle occurs with declared functions.
Interestingly, a variable is created with the same name as the function.

## Function expression
A function expression looks like this:
    var example = function() {}
This kind of function is evaluated at run-time. example can't be called until it the JS engine has reached that code. If it's called at some point beforehand, you'll get an error.

In reality, they're incredibly similar functionality wise. Just make sure you're aware of how the Javascript interpreter is going to load them.

## Function constructor
This is a concept that was new to me before writing this - so perhaps the self-documentation idea does have merits!
It is possible to write:
    var example = new Function() {}
Mozilla's Developer Network advises against this approach because:
> it needs the function body as a string, which may prevent optimizations

Douglas Crockford recommends that JS authors use function expressions because
> it makes it clear that the variable contains a function value

From writing my own code and working with others', I prefer the aesthetics of the function expression: it's much easier to read at a glance and determine what functionality is available.

However, it appears there are a number of subtle differences which may crop up later in the development cycle:
* A function name cannot be changed, but a variable to which a function is assigned _can_ be reassigned.
* The function name can only be used within the function's body.