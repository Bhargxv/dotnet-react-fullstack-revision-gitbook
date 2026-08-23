# 16. `fetch` & HTTP Requests

`fetch()` is the browser's built-in API for making HTTP requests.

``` js
const response = await fetch("/api/users");
```

`fetch()` returns a Promise that resolves to a `Response` object.

By default:

``` js
fetch("/api/users");
```

performs a GET request.

For POST:

``` js
fetch("/api/users", {
    method: "POST"
});
```

------------------------------------------------------------------------

## `Response` vs actual data

This distinction is important.

``` js
const response = await fetch(url);
```

`response` is the HTTP `Response` object.

It contains things such as:

``` js
response.status
response.ok
response.headers
```

The actual JSON body is obtained with:

``` js
const users = await response.json();
```

Mental model:

``` text
fetch()
   ↓
Promise<Response>
   ↓ await
Response object
   ↓ response.json()
Promise<data>
   ↓ await
Actual JavaScript data
```

------------------------------------------------------------------------
