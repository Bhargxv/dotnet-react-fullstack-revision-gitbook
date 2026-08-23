# 6. Arrow Functions

Traditional function:

``` js
function square(number) {
    return number * number;
}
```

Arrow function with block body:

``` js
const square = (number) => {
    return number * number;
};
```

Arrow function with implicit return:

``` js
const square = (number) => number * number;
```

**Important:**

Arrow functions do not have their own `this`; they inherit `this` from
the surrounding lexical scope.

This differs from regular functions.

------------------------------------------------------------------------
