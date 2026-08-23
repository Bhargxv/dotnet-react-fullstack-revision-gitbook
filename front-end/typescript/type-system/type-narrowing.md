# 30. Type Narrowing

When a value has a union type, TypeScript can narrow it after checking.

``` ts
function formatId(id: number | string) {
    if (typeof id === "number") {
        return "Number: " + id;
    }

    return "String: " + id.toUpperCase();
}
```

Before the check:

``` text
id → number | string
```

Inside the `if`:

``` text
id → number
```

After the `if`:

``` text
id → string
```

**Definition:**

> Type narrowing is the process of using runtime checks to reduce a
> union to a more specific type.

**Memory hook:**

> Check the type → TypeScript narrows the type.

------------------------------------------------------------------------
