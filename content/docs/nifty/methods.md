---
title: "Struct Methods"
weight: 9
---

## Impl

Nifty allows for methods to be added to structs.

For methods the `md` keyword is used so that if the `impl` keyword is missed by a programmer or a programmer 
jumps to the middle of the file it is obvious that these are methods and not ordinary functions. The `fn` 
keyword can be used as well if preferred. The `md` keyword can't be used outside an `impl`.

![impl](/images/impl.svg)

Receiver objects can be explicetly passed to methods. See the `Receiver Argument` section.

![impl_init](/images/impl_init.svg)

You may have noticed that I used both `->` and `.` when calling the functions. Nifty works like c++ in that 
objects that are pointers use `->` and objects that are not pointers use `.` instead. This is to visually 
distinguish the two.

## Constimpl

A struct can be implemented multiple times. So for instance a struct could exist in a library and you could 
extend it in you own code.

![impl_multiple](/images/impl_multiple.svg)

To prevent this the `constimpl` keyword can be used.

![impl_const](/images/impl_const.svg)

Multiple `constimpl` can be used within the orginal file the struct is defined in. With generics there are cases 
where it may make sence to have seperate implementations for different types.

## Receiver Argument

When implementing functions on a struct the structs fields are implicitly available to the function body. Optionally 
functions implemented on a struct can have a receiver argument. The receiver argument is in brackets right before 
the functions parentheses. The struct type name can be used for the type.

![impl_receiver](/images/impl_receiver.svg)

