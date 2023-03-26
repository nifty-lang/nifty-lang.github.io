---
title: "Types"
weight: 3
---

## Basic Types

```nifty
char // same as u32 defaults to '\0'
int // same as s32 defaults to 0
uint // same as u32 defaults to 0
float // same as f32 defaults to 0.f
double // same as f64 defaults to 0.d

uintptr // defaults to 0

// defaults to false
bool b8 b16 b32 b64

// defaults to 0
u8 u16 u32 u64 u128
s8 s16 s32 s64 s128

//defaults to 0.0
f16 f32 f64 f128

//defaults to ""
string

// defaults to "\0"
cstring // Null terminated string. Meant for interfacing with c libraries.

typeid // runtime identifier for a type.

rawptr // Like void* in c, used for compatibility with existing c code.
```

## Type Aliases

Type aliases can be created with the `type ... as` pattern.

```nifty
type Month as int
```

To force a type alias to be distinct, use the distinct attribute.

```nifty
#[distinct] type Month as int
```
