---
title: "Getting Started"
weight: 1
---

Nifty is a simple and easy language to get started with. Let's go!

## Downloading Nifty

Download nifty for your platform [here](https://github.com/ATSOTECK/nifty/releases).

If you want to build and install nifty yourself see the `README` in the repo for instructions.

## Syntax Highlighting

We have a plugin for Visual Studio Code that will make developing nifty programs nicer. Search for an extension called nifty-lang and install it. There is also a vim theme available on github as well.

## Hello World

Once everything is installed let's make a simple nifty program to make sure it's installed correctly.

```sh
mkdir hello
cd hello
nifty new
```

Nifty will generate a file called `build.toml` and a file called `hello.nifty` which should look like this:

```nifty
package hello

using <fmt>

fn main() {
    println("Hullo!")
}
```

To build and run the project use:

```sh
nifty run hello
```

This will build and then run the `hello` target in `build.toml`.

Because hello is the default target in the project you can also run it with:

```sh
nifty run
```

Or even just:

```sh
nifty
```

By default nifty will try to build and run the default target in `build.toml` when called.

If you just want to build the project use:
```sh
nifty build hello
```
