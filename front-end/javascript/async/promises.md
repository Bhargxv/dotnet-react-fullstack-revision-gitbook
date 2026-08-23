# 14. Promises

**Definition:**

> A Promise represents the eventual result of an asynchronous operation.
> It can be pending, fulfilled, or rejected.

States:

``` text
Pending
   ↓
Fulfilled
   OR
Rejected
```

Example:

``` js
const promise = new Promise((resolve, reject) => {
    resolve("Success!");
});
```

`resolve(value)` means success.

`reject(error)` means failure.

------------------------------------------------------------------------

## `.then()` and `.catch()`

``` js
promise
    .then(result => {
        console.log(result);
    })
    .catch(error => {
        console.log(error);
    });
```

`.then()` handles fulfillment.

`.catch()` handles rejection.

**C# analogy:**

``` text
Promise<T> ≈ Task<T>
await Promise ≈ await Task
```

This is a conceptual analogy, not a statement that the implementations
are identical.

------------------------------------------------------------------------
