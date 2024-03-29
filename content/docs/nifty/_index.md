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

Follow the interactive project creation dialog.

Nifty will generate a file called `build.toml` and a file called `hello.nifty` (or whatever you decided to call it) which should look like this:

![hello_world](/images/hello_world.svg)

To build and run the project use:

```sh
nifty run hello
```

This will build and then run the `hello` target in `build.toml`.

Because `hello` is the default target in the project you can also run it with:

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

## Comments

Comments are sismilar to comments in other c-like languages. Nifty allows for nested comments.

![comments](/images/comments.svg)

Nifty style multiline comments require one less key press. I did say I'm lazy.

{{< button "variables" "Next: Variables" >}}
