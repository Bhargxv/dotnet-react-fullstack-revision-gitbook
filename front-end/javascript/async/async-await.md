# 15. `async/await`

`async/await` provides cleaner syntax for working with Promises.

``` js
async function loadUser() {
    const user = await getUser();
    console.log(user);
}
```

An `async` function returns a Promise.

`await` waits for the Promise's result and pauses the current async
function until the Promise settles.

**Important correction:**

> `await` does not block/freeze the entire JavaScript thread.

It pauses the current async function while other JavaScript work can
continue.

------------------------------------------------------------------------

## Mental model

``` text
Start async operation
        ↓
await
        ↓
pause this async function
        ↓
other JavaScript can run
        ↓
Promise settles
        ↓
resume async function
```

------------------------------------------------------------------------
