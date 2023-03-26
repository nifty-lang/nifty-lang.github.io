---
title: "Variables"
weight: 2
---

Variables in nifty work a little bit differently than in other languages.

## Variables

Variables are declared with the `let` keyword.

```rust
let x: int = 12
```

The types can be inferred.

```rust
let x = 12 // x is an int.
let y = someFunc()
```

The variable declaration operator can be used as well.

```go
a := 12   // x is an int.
b := 12.f // b is a float/f32.
c := 12.0 // c is a float/f32.
d := 12.d // d is a double/f64.
```

By default variables in nifty are initialized to their zero value.
```rust
let x: int // x is 0.
```

Variables can be explicitly be uninitialized with the `undefined` keyword or with `#noAutoInit`.
```rust
let a: int = undefined
#noAutoInit {
    let x: int
    let y: float
    let z: string
}
b := a // Valid, but undefined behavior.
```

Undefined can only be used for declaration.

```rust
let x = 12
x = undefined // Invalid!
if (x == undefined) // Invalid!
```

Nifty does not support variable shadowing.

```rust
let x: int
{
    let x: float // Invalid!
}
```

## Runtime Constants

Runtime constants are declared with the 'val' keyword.

```kotlin
val x: int = 12
```

Type infence can be used as well.

```kotlin
val x = 12
val y = someFunc()
```

The constant declaration operator can be used as well.

```rust
x ::= 12
y ::= someFunc()
```

The `undefined` keyword can't be used with constants. Constants do not have zero values and their values must be specified.

```kotlin
val x: int = undefined // Invalid!
val y: int // Invalid!
```

## Compiletime Constants

Compiletime constants are declared with the `const` keyword and their value must be known at compiletime. Type inference works with compiletime consts and the constant declaration operator can be used with compiletime consts. The compiler will decide if something is a runtime or compiletime const so the same operator can be used.

```rust
const x: int = 12
const y = someFunc() // Invalid!
const z = 42
const a = #SOME_MACRO_CONST
b ::= 19
```

## Unused

If a function returns two or more variables and you don't care about all of them you can use `unused`.

```go
x, unused := someFunc()
unused, y := someFunc()
```

If a function is marked with `#[useReturn]` then `unused` can be used to ignore the result.

```go
unused := useReturnFunc()
```

`unused` can't be a constant.

```rust
unused ::= someFunc() // Invalid!
```

`unused` is not a real variable.

```go
x := unused // Invalid!
fmt::println(unused) // Invalid!
type_of(unused) // Invalid!
```
