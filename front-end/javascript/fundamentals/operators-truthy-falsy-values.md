# 3. Operators & Truthy/Falsy Values

## `+`

For numbers:

``` js
10 + 5; // 15
```

For strings, `+` can concatenate:

``` js
"Hello " + "Sunny"; // "Hello Sunny"
```

JavaScript performs type coercion in some expressions:

``` js
"10" + 5; // "105"
```

The `+` operator with a string operand can result in string
concatenation.

------------------------------------------------------------------------

## Truthy and Falsy

JavaScript converts values to boolean context.

Common falsy values:

``` text
false
0
-0
0n
""
null
undefined
NaN
```

Most other values are truthy, including:

``` js
[]
{}
"0"
"false"
```

**Memory hook:**

> Empty string, zero, null, undefined, false and NaN are falsy.

------------------------------------------------------------------------

## `&&` and `||` return values

These operators do not necessarily return `true` or `false`.

### `&&`

Returns the first falsy value; otherwise returns the last value.

``` js
const result = "Hello" && "World";
// "World"
```

``` js
const result = 0 && "Hello";
// 0
```

### `||`

Returns the first truthy value; otherwise returns the last value.

``` js
const result = "" || "Guest";
// "Guest"
```

``` js
const result = "Sunny" || "Guest";
// "Sunny"
```

**Memory hook:**

> `&&` looks for the first falsy value.

> `||` looks for the first truthy value.

------------------------------------------------------------------------
