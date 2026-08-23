# 26. Optional Properties

Use `?` for an optional property:

``` ts
interface User {
    id: number;
    name: string;
    email?: string;
}
```

Valid:

``` ts
const user: User = {
    id: 1,
    name: "Sunny"
};
```

Also valid:

``` ts
const user: User = {
    id: 2,
    name: "Rahul",
    email: "rahul@example.com"
};
```

But:

``` ts
email: 123
```

is invalid because if `email` exists, it must be a string.

**Memory hook:**

> `email?: string` = string or absent.

------------------------------------------------------------------------
