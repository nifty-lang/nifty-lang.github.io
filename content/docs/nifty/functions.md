---
title: "Functions"
weight: 4
---

## Function Basics

Like many other programming language nifty has functions.

![functions1](/images/functions1.svg)

Functions in nifty work a bit differently compared to languages like c/c++.

![functions2](/images/functions2.svg)

## Variadic Functions

Functions in nifty can be `variadic`, meaning they can take a variable number of arguments.

![vary](/images/vary.svg)

Did you know that a function with 9 arguments is called Novenary? Well now you do!

## Function Overloading

Nifty has function overloading, but it works differently compared to languges like c++. 
Instead of two functions having the same name but different arguments the functions have different names and are explicetly overloaded. 

For instance if you had a `pow` function for `int`, `float`, and `double` it might look like this:

![overload](/images/overload.svg)

## Function Attributes

Function in nifty can have attribues that give the function certain requirements or just gives the compiler more information about the function.

For instance if you wanted to require a return value must be used you can like this:

![use_return](/images/use_return.svg)

Functions can have preconditions or postconditions.

![use_return](/images/conditions.svg)

Note that if `in` is used and the pointer is passed to second function that second function may be able to 
write to the pointer unless it also has the `in` restriction. `in` only guarantees that the function 
it is applied to won't directly write to the pointer. Same issue with `out`.

Here are some more examples of function attributes.

![attrib_examples](/images/attrib_examples.svg)

You have access to the function attribues via reflection.

Here is a list of built-in function attributes.

``` 
useReturn
optionalOk
minArity(argc: int)
maxArity(argc: int)
deprecated(msg: string = "")
deprecatedAfter(date: string) // yyyy-mm-dd
maybeUnused
warning(msg: string)
static // Like static in c/c++.
requireTargetFeature(feature: string)
noReturn
asmReturn // Indicates that the function returns via inline assembly instead of a return statement.
inline
noInline
maybeInline
noContext
traceVars(names: ..string) // Prints the values of the variables listed every time they change.
                           // This is meant for debugging and will be relatively slow.

signal
slot

The following are called at the end of the callers scope.
deferredIn(function: fn) // Receives the same paramaters as the called function.
deferredOut(function: fn) // Receives the results of the called function.
deferredInOut(function: fn) // Receives both the input and output of the called function.
deferredNone(function: fn) // Receives no input.
These can be useful but are not always recommended as they can make it not obvious why a function
is being called without further investigation. May get rid of these.

linkName(name: string)

require {code}
ensure {code}
in(vars: ..string)
out(vars: ..string)
inout(vars: ..string)
```
