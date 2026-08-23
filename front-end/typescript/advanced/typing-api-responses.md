# 32. Typing API Responses

Suppose an API returns:

``` json
{
    "id": 101,
    "name": "Sunny",
    "email": "sunny@example.com"
}
```

Define:

``` ts
interface User {
    id: number;
    name: string;
    email: string;
}
```

Then:

``` ts
async function getUser(): Promise<User> {
    const response = await fetch("/api/user");

    if (!response.ok) {
        throw new Error("Failed to fetch user");
    }

    return await response.json();
}
```

Now:

``` ts
const user = await getUser();

user.id;
user.name;
user.email;
```

TypeScript knows the expected return shape.

**Important correction:**

Typing a function as:

``` ts
Promise<User>
```

does not automatically validate the actual runtime JSON returned by the
server.

TypeScript is primarily providing compile-time information.

**Memory hook:**

> `Promise<User>` = this async operation is expected to produce a
> `User`.

------------------------------------------------------------------------
