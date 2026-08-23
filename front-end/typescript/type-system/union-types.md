# 28. Union Types

A union means a value can be one of several allowed types or values.

``` ts
type Status = "loading" | "success" | "error";
```

Valid:

``` ts
let status: Status;

status = "loading";
status = "success";
status = "error";
```

Invalid:

``` ts
status = "pending";
```

Another example:

``` ts
function printId(id: number | string) {
    // id can be number or string
}
```

**Memory hook:**

> `A | B` = A OR B.

------------------------------------------------------------------------
