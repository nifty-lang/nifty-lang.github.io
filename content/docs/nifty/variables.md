---
title: "Variables"
weight: 2
---

Variables in nifty work a little bit differently than in other languages.

## Variables

Variables are declared with the `let` keyword.

![let](/images/let.svg)

By default variables in nifty are initialized to their `zero` value.

![undefined](/images/undefined.svg)

Nifty does not support variable shadowing.

![shadow](/images/shadow.svg)

## Runtime Constants

Runtime constants are declared with the `val` keyword.

![val](/images/val.svg)

## Compiletime Constants

Compiletime constants are declared with the `const` keyword and their value must be known at compiletime. Type inference works with compiletime consts and the constant declaration operator can be used with compiletime consts. The compiler will decide if something is a runtime or compiletime const so the same operator can be used.

![const](/images/const.svg)

## Unused

If a function returns two or more variables and you don't care about all of them you can use `unused`.

![unused](/images/unused.svg)
