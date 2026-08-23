# 25. Interfaces

An interface describes the shape/contract of an object.

``` ts
interface Product {
    id: number;
    name: string;
    price: number;
    inStock: boolean;
}
```

Then:

``` ts
const product: Product = {
    id: 1,
    name: "Laptop",
    price: 999.99,
    inStock: true
};
```

TypeScript checks that the object follows the interface.

**Memory hook:**

> Interface = object shape/contract.

------------------------------------------------------------------------
