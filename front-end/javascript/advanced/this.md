# 21. `this`

For a regular method call:

``` js
const user = {
    name: "Sunny",

    greet() {
        console.log(this.name);
    }
};

user.greet();
```

`this` refers to `user` in this call.

So:

``` js
this.name
```

is effectively:

``` js
user.name
```

------------------------------------------------------------------------

## `this` depends on how a regular function is called

``` js
const user1 = {
    name: "Sunny",

    greet() {
        console.log(this.name);
    }
};

const user2 = {
    name: "Rahul",
    greet: user1.greet
};

user1.greet(); // Sunny
user2.greet(); // Rahul
```

The same function is called with different receivers.

**Memory hook:**

> For a regular method call, think: "Who called me?"

------------------------------------------------------------------------

## Arrow functions and `this`

Arrow functions do not create their own `this`.

They inherit `this` from the surrounding lexical scope.

**Interview trap:**

> Don't say arrow functions dynamically determine `this` from the
> calling object.

------------------------------------------------------------------------
