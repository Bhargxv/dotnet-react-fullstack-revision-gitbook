# 8. `map`, `filter`, `find`

## `map`

**Definition:**

> `map()` transforms every element and returns a new array of the
> transformed values.

``` js
const numbers = [10, 20, 30];

const doubled = numbers.map(n => n * 2);
// [20, 40, 60]
```

Mental model:

``` text
every item → transform → new array
```

------------------------------------------------------------------------

## `filter`

**Definition:**

> `filter()` keeps elements that satisfy a condition and returns a new
> array.

``` js
const numbers = [10, 20, 30, 40];

const result = numbers.filter(n => n >= 25);
// [30, 40]
```

Mental model:

``` text
every item → condition → keep/discard
```

------------------------------------------------------------------------

## `find`

**Definition:**

> `find()` returns the first element that satisfies a condition.

``` js
const users = [
    { id: 1, name: "Rahul" },
    { id: 2, name: "Sunny" }
];

const user = users.find(u => u.id === 2);
// { id: 2, name: "Sunny" }
```

If no match exists, `find()` returns `undefined`.

**Memory hook:**

> `map` = transform all.

> `filter` = keep matching all.

> `find` = find first match.

------------------------------------------------------------------------
