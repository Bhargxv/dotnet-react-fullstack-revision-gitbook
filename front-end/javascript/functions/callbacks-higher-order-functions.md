# 12. Callbacks & Higher-Order Functions

## Callback

**Definition:**

> A callback is a function passed into another function so that the
> receiving function can invoke it.

Example:

``` js
const add = (a, b) => a + b;

function calculate(a, b, operation) {
    return operation(a, b);
}

const result = calculate(10, 20, add);
// 30
```

Here:

``` text
calculate = higher-order function
add = callback
operation = parameter referencing the callback
```

**Memory hook:**

> Callback = function passed to another function.

------------------------------------------------------------------------

## Higher-Order Function

**Definition:**

> A higher-order function is a function that accepts another function
> and/or returns a function.

Examples:

``` js
map()
filter()
find()
```

all commonly receive callbacks.

------------------------------------------------------------------------
