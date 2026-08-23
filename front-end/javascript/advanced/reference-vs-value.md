# 20. Reference vs Value

Primitive values behave like independently copied values:

``` js
let a = 10;
let b = a;

b = 20;

// a = 10
// b = 20
```

Objects and arrays are reference values.

``` js
const user1 = {
    name: "Sunny"
};

const user2 = user1;

user2.name = "Rahul";

console.log(user1.name);
// "Rahul"
```

Both variables refer to the same object.

``` text
user1 ──┐
        ↓
      Object
        ↑
user2 ──┘
```

------------------------------------------------------------------------

## Creating a new object with spread

``` js
const user1 = {
    name: "Sunny",
    age: 25
};

const user2 = {
    ...user1
};

user2.age = 30;
```

Now:

``` text
user1.age → 25
user2.age → 30
```

**Memory hook:**

> Same reference → shared mutation.

> Spread → new top-level object/array.

------------------------------------------------------------------------
