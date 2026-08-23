# 19. Closures

**Definition:**

> A closure is a function that retains access to variables from its
> surrounding lexical scope even after the outer function has finished
> executing.

Example:

``` js
function createCounter() {
    let count = 0;

    return function () {
        count++;
        return count;
    };
}

const counter = createCounter();

console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
```

`counter` stores the function returned by `createCounter()`.

The returned function remembers the `count` variable.

**Mental model:**

``` text
createCounter()
      ↓
count = 0
      ↓
returns function
      ↓
counter stores function
      ↓
counter() executes it
      ↓
function remembers count
```

Two calls to `createCounter()` create separate closures:

``` js
const counter1 = createCounter();
const counter2 = createCounter();
```

They have independent `count` variables.

**Why it matters:**

Closures appear frequently in callbacks and React code, especially with
hooks and event handlers.

**Memory hook:**

> Closure = function + remembered surrounding variables.

------------------------------------------------------------------------
