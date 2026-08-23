# 13. JavaScript Modules

Modules allow code to be split across files.

## Named export

``` js
// math.js
export function add(a, b) {
    return a + b;
}

export function multiply(a, b) {
    return a * b;
}
```

Import:

``` js
import { add, multiply } from "./math.js";
```

Named exports use curly braces.

------------------------------------------------------------------------

## Default export

``` js
// UserCard.jsx
export default UserCard;
```

Import:

``` js
import UserCard from "./UserCard";
```

Default imports do not require curly braces.

**Memory hook:**

> Named export → `{ name }`.

> Default export → `name`.

------------------------------------------------------------------------
