# 5. Functions

A function groups reusable behavior.

``` js
function greet(name) {
    return "Hello, " + name;
}

const message = greet("Sunny");
```

**Definition:**

> A function is a reusable block of behavior that can accept inputs
> (parameters) and optionally return a value.

**Parameter vs argument:**

``` js
function greet(name) {   // name = parameter
    return "Hello " + name;
}

greet("Sunny");          // "Sunny" = argument
```

**Memory hook:**

> Parameter = placeholder.

> Argument = actual value supplied.

------------------------------------------------------------------------
