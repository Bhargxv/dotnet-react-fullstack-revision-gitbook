# 2. `const` vs Object/Array Mutation

Consider:

``` js
const fruits = ["apple", "banana"];

fruits.push("mango"); // valid
```

But:

``` js
fruits = ["orange"]; // invalid
```

Why?

`fruits` still points to the same array. `push()` mutates that array.

Similarly:

``` js
const user = {
    name: "Sunny"
};

user.name = "Rahul"; // valid
```

But:

``` js
user = {
    name: "Rahul"
}; // invalid
```

**Interview answer:**

> `const` prevents reassignment of the variable binding, but it does not
> make referenced objects or arrays immutable.

------------------------------------------------------------------------
