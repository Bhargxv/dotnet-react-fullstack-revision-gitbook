# 27. `type` Aliases

Type aliases can define named types.

``` ts
type User = {
    id: number;
    name: string;
};
```

For simple object shapes, `type` and `interface` can look very similar.

A practical rule:

> Use `interface` commonly for object/class-like contracts. Use `type`
> when you need flexible type composition such as unions and
> intersections.

Example:

``` ts
type Status = "loading" | "success" | "error";
```

------------------------------------------------------------------------
