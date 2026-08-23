# 18. Scope

**Definition:**

> Scope determines where a variable can be accessed.

Example:

``` js
const company = "Example";

function employee() {
    const name = "Sunny";

    function printDetails() {
        console.log(company);
        console.log(name);
    }

    printDetails();
}
```

`printDetails()` can access variables from its own scope and outer
scopes.

This is the **scope chain**.

------------------------------------------------------------------------

## Block scope

`let` and `const` are block-scoped.

``` js
if (true) {
    const message = "Hello";
}

console.log(message); // error
```

`var` is function-scoped and behaves differently.

**Modern practice:**

> Prefer `const`, use `let` when reassignment is needed, and generally
> avoid `var`.

------------------------------------------------------------------------
