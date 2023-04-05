---
title: "Behaviors"
weight: 10
---

## Basics

Behaviors are a a way to define shared behavior. To indicate that an implementation does a certain behavior 
the `does` keyword is used. Implementations can do one or more behaviors.

If an implementation does a behavior then all the functions in the behavior must be implemented or there will 
be a compiler error. If an implementation does multiple behaviors with conflicting function names then 
there will be a compiler error. If a behavior and an impl have conflicting function names there will be a 
compiler error. These errors can be fixed by prefixing with `BehaviorName::` to remove ambiguity. See example below.

![behavior](/images/behavior.svg)

## As Types

Behaviors can be used as types for parameters to define a function that can take many types that all share that behavior.

![behavior_arg](/images/behavior_arg.svg)


Behaviors can be combined into new behviors via type intersections.

![behavior_and](/images/behavior_and.svg)

Type intersections can only be used with behaviors.

## Conflicts

If two behaviors have conflicting symbols then the name of the bahavior must be used.

![behavior_conflict](/images/behavior_conflict.svg)

## Default Implementations

Behaviors can have overridable default function implementations.

![behavior_default](/images/behavior_default.svg)

## Printable Struct

To print a struct type use the `fmt::Printable` behavior.

![printable](/images/printable.svg)
