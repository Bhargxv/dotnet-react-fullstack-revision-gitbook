# 11. Spread & Rest

## Spread

Spread expands values into a new structure.

Object:

``` js
const user = {
    name: "Sunny",
    age: 25
};

const updatedUser = {
    ...user,
    age: 26
};
```

`updatedUser` is a new top-level object.

Array:

``` js
const numbers = [1, 2, 3];

const newNumbers = [...numbers, 4, 5];
```

**Mental model:**

> Spread = take the contents and place them into a new structure.

------------------------------------------------------------------------

## Rest

Rest collects remaining values.

``` js
function printNumbers(first, ...rest) {
    console.log(first);
    console.log(rest);
}

printNumbers(10, 20, 30, 40);
```

Output conceptually:

``` text
10
[20, 30, 40]
```

**Memory hook:**

> Spread = expand.

> Rest = collect.

------------------------------------------------------------------------

## Shallow copy

Spread creates a shallow copy.

``` js
const user1 = {
    name: "Sunny",
    address: {
        city: "Vizag"
    }
};

const user2 = {
    ...user1
};
```

The outer objects are different, but the nested `address` object is
still shared.

Therefore:

``` js
user2.address.city = "Hyderabad";

console.log(user1.address.city);
// "Hyderabad"
```

**Interview trap:**

> Do not say spread creates a completely independent deep copy.

------------------------------------------------------------------------
