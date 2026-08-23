# 24. TypeScript Basic Types & Type Inference

Explicit typing:

``` ts
const age: number = 25;
const name: string = "Sunny";
const active: boolean = true;
```

But TypeScript can infer obvious types:

``` ts
const age = 25;
const name = "Sunny";
const active = true;
```

This is **type inference**.

**Best practice:**

> Don't add explicit types when TypeScript can infer them clearly,
> unless the annotation communicates an important contract.

------------------------------------------------------------------------
