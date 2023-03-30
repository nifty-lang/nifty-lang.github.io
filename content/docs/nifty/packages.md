---
title: "Packages"
weight: 10
---

## Intro

All nifty programs are made of packages.

The Nifty Standard Library (`nsl`) has many built-in packages.

![packages1](/images/packages1.svg)

It is fine to just use the default package for your programs. By default the default package is empty. 
Just using the default package could be an issue for larger programs though. 
The default package can't be imported and can't be used for packages meant to be used as 3rd party packages.

## Use As

By default the name of the package is the last element of the package path, which is also the name of the package
 in the file. This, however, can be changed with the `as` keyword

![packages2](/images/packages2.svg)

## Access Level

In nifty all items not starting or ending with an underscore are exported from the package. You can think of them as public.

Items that start with an underscore are not exported and are private to the package.

Items that end with an underscore are not exported and are private to the file they are in.

![packages3](/images/packages3.svg)

## Header Files

Header files? In 2023?!? Apparently I'm the only one in the world that actually likes header files. So they are in nifty. However they are very different from header files in c/c++ and they are completely optional.

In nifty instead of being called header files they are called api files. A package may have at most one api file. Api files should be named like `package_name.api.nifty`. For example for a `game` package it would be `game.api.nifty`. The api file must be in the same folder as the package for development. Using a package with an api file works just like any other package. Everything in the api file must be defined/implemented in the package.

Api files can be used to expose an api for your package without exposing the implementation. Or sometimes it's just nice to peruse the contents of the package without the implementation details getting in the way. Api files could also be where the documentation is written so it doesn't get in the way of the implementation details.

![api](/images/api.svg)
