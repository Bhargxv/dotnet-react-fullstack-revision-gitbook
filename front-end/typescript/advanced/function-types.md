# 29. Function Types

Functions can themselves have types.

``` ts
type Operation = (a: number, b: number) => number;
```

This means:

``` text
two number parameters
        ↓
returns number
```

Valid:

``` ts
const add: Operation = (a, b) => a + b;

const multiply: Operation = (a, b) => a * b;
```

Invalid:

``` ts
const greet: Operation = (name) => {
    return "Hello " + name;
};
```

The return value is a string, while `Operation` requires a number.

**Memory hook:**

> Function type = input parameter types + return type.

------------------------------------------------------------------------
