---
title: "Arrays"
weight: 7
---

Nifty has two types of arrays, static and dynamic.

## Static

Static arrays can't have item added or removed from them. Their size is fixed and determined at compile time.

![static_arrays](/images/static_arrays.svg)

## Dynamic

Dynmic arrays can have item added or removed from them. Their size can be set at compile time but is not fixed.

![dynamic_arrays](/images/dynamic_arrays.svg)

## Use

Like most other programming languages arrays in nifty are zero indexed.

![arrays](/images/arrays.svg)

More information on the array API will be available in the Nifty Standard Library (nsl) documentation.

## Slices

Slices are like arrays but can be more accurately thought of as a view into the array.
A slice is created by specifying the start index and the end index. Slices can be used on both static and dynamic arrays.

![slices](/images/slices.svg)
