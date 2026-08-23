# 10. Destructuring

Destructuring extracts values from objects or arrays.

## Object destructuring

``` js
const employee = {
    name: "Rahul",
    age: 28,
    role: "Developer"
};

const { name, age, role } = employee;
```

This does not mutate the original object.

You can rename during destructuring:

``` js
const { name: employeeName } = employee;
```

------------------------------------------------------------------------

## Array destructuring

``` js
const numbers = [10, 20, 30];

const [first, second] = numbers;
```

`first` becomes `10`, `second` becomes `20`.

**Memory hook:**

> Destructuring = extract values from an existing structure.

------------------------------------------------------------------------
