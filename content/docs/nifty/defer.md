---
title: "Defer"
weight: 6
---

## Normal

Nifty has defer.

`defer` defers the execution of code until the end of the current scope.

![defer](/images/defer.svg)

## Error

Nifty has a second type of defer, `defer_err`. `defer_err` only runs if the function returns an error.
This can only be used in function that returns a `Result`. This is because if the function returns
an `Errorable` then it would always be called because the function would always have to return an
`Errorable`. In that case defer should be used. `defer_err` is run in a FILO fashion as well.

![defer_err](/images/defer_err.svg)
