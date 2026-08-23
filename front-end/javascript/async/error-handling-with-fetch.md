# 17. Error Handling with `fetch`

## HTTP errors

A common trap:

> `fetch()` does not automatically reject its Promise for HTTP 404 or
> 500 responses.

Example:

``` js
const response = await fetch("/api/users");

if (!response.ok) {
    throw new Error("Failed to fetch users");
}
```

`response.ok` is generally true for successful HTTP status codes and
false for unsuccessful ones.

Then:

``` js
try {
    const response = await fetch("/api/users");

    if (!response.ok) {
        throw new Error("Failed to fetch users");
    }

    const users = await response.json();
}
catch (error) {
    console.log(error);
}
```

------------------------------------------------------------------------

## Network failure vs HTTP failure

Network-level failure:

``` text
No usable HTTP response
        ↓
Promise rejects
        ↓
catch
```

HTTP error:

``` text
404 / 500
        ↓
fetch resolves with Response
        ↓
response.ok === false
        ↓
throw manually
        ↓
catch
```

**Interview trap:**

> Don't say "fetch throws automatically for 404/500."

------------------------------------------------------------------------
