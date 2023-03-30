---
title: "Control Flow"
weight: 5
---

## Parentheses and Braces

Curly braces `{` `}` are required for all control flow. The parentheses `(` `)` are optional.

## For

![for](/images/for.svg)

## While

![while](/images/while.svg)

## Until

![until](/images/until.svg)

## When

![when](/images/when.svg)

## If

![if](/images/if.svg)

## Ternary operator

![ternary](/images/ternary.svg)

## Goto

![goto](/images/goto.svg)

By default `goto` is disabled by the compiler. This can be enabled in `build.toml`.

![goto_xkcd](/images/goto.png)

## Continue and Break

![continue_break](/images/continue_break.svg)

## Labelled Blocks

![labelled_blocks](/images/labelled_blocks.svg)

## Block Values

Blocks are expressions and can be used to get values.

Sometimes it's impracticle or not possible to initialize/set a variable in one line. Using blocks can prevent needing to set the variable to undefined or a temporary value.

Blocks can be labbeled as well to return a value from a specified block if nested.

![block_values](/images/block_values.svg)
