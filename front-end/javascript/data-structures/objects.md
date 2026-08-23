# 9. Objects

Objects represent collections of named properties.

``` js
const employee = {
    name: "Rahul",
    age: 29,
    role: "Developer"
};
```

Access:

``` js
employee.name;
employee["age"];
```

Properties can be mutated:

``` js
employee.age = 30;
```

With `const`, the binding is fixed but the object can still be mutated.

------------------------------------------------------------------------
