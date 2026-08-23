# 1. JavaScript Variables & Types

## `let` and `const`

**Definition:**

`let` and `const` declare block-scoped variables in JavaScript.

`let` allows reassignment. `const` does not allow reassignment of the
variable binding.

``` js
let score = 0;
score = 10; // valid

const age = 25;
age = 30; // error
```

**Why it matters:**

Modern JavaScript generally uses `const` by default and `let` when
reassignment is required.

**Mental model:**

> `const` = the variable cannot be pointed at a different value.

> `let` = the variable can be reassigned.

**Important correction:**

`const` does **not** make objects or arrays immutable.

``` js
const user = {
    name: "Sunny"
};

user.name = "Rahul"; // valid

// user = {}; // invalid
```

The object can be mutated, but the `user` variable cannot be reassigned
to another object.

**Memory hook:**

> `const` protects the binding, not the object.

------------------------------------------------------------------------

## JavaScript Primitive Types

Common primitive types:

``` text
number
string
boolean
undefined
null
bigint
symbol
```

Examples:

``` js
const age = 25;             // number
const name = "Sunny";       // string
const active = true;        // boolean
let value;                  // undefined
const selected = null;      // null
```

Objects, arrays and functions are non-primitive/reference-type values.

------------------------------------------------------------------------

## `undefined` vs `null`

**`undefined`:**

Usually means a value has not been assigned or a value/property is
absent.

``` js
let value;
console.log(value); // undefined
```

**`null`:**

An explicit assignment representing "no value".

``` js
const selectedUser = null;
```

**Memory hook:**

> `undefined` = not provided/assigned.

> `null` = intentionally no value.

------------------------------------------------------------------------
