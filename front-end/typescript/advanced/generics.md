# 31. Generics

**Definition:**

> Generics allow reusable code to work with different types while
> preserving type information.

Basic example:

``` ts
function identity<T>(value: T): T {
    return value;
}
```

Usage:

``` ts
const a = identity(100);       // number
const b = identity("Hello");   // string
const c = identity(true);      // boolean
```

TypeScript infers `T` from the argument.

C# analogy:

``` csharp
T Identity<T>(T value)
{
    return value;
}
```

**Memory hook:**

> Generic `T` = type placeholder.

------------------------------------------------------------------------
