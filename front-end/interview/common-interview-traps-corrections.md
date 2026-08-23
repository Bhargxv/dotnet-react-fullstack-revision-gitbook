# 36. Common Interview Traps & Corrections

### Trap 1

> "const makes objects immutable."

**Correction:**

> `const` prevents reassignment of the variable binding; the referenced
> object can still be mutated.

------------------------------------------------------------------------

### Trap 2

> "All JavaScript async code runs on another thread."

**Correction:**

> JavaScript's asynchronous behavior is coordinated through the
> runtime's event loop and related mechanisms. Don't reduce it to
> "everything runs on another thread."

------------------------------------------------------------------------

### Trap 3

> "await blocks JavaScript."

**Correction:**

> `await` pauses the current async function while allowing other
> JavaScript work to continue.

------------------------------------------------------------------------

### Trap 4

> "fetch throws when the server returns 404."

**Correction:**

> `fetch` normally resolves with a Response for HTTP error statuses.
> Check `response.ok`.

------------------------------------------------------------------------

### Trap 5

> "Spread creates a deep copy."

**Correction:**

> Spread creates a shallow copy. Nested objects can still share
> references.

------------------------------------------------------------------------

### Trap 6

> "A closure is just an inner function."

**Correction:**

> A closure is a function together with access to variables from its
> surrounding lexical scope.

------------------------------------------------------------------------

### Trap 7

> "Arrow functions have their own this."

**Correction:**

> Arrow functions don't create their own `this`; they inherit it from
> the surrounding lexical scope.

------------------------------------------------------------------------

### Trap 8

> "TypeScript guarantees runtime type safety."

**Correction:**

> TypeScript provides static type checking during development/build
> time. It does not automatically validate arbitrary runtime data such
> as API responses.

------------------------------------------------------------------------

### Trap 9

> "Optional property means it can have any type."

**Correction:**

``` ts
email?: string
```

means the property can be absent; if present, it should be a string.

------------------------------------------------------------------------

### Trap 10

> "Generics are the same as any."

**Correction:**

> Generics preserve type information. `any` largely disables type
> checking for that value.

------------------------------------------------------------------------

# Final Memory Map

``` text
JAVASCRIPT
│
├── Variables & Types
│   ├── let
│   ├── const
│   ├── primitives
│   └── truthy/falsy
│
├── Functions
│   ├── normal functions
│   ├── arrow functions
│   ├── callbacks
│   └── higher-order functions
│
├── Collections
│   ├── arrays
│   ├── map
│   ├── filter
│   ├── find
│   ├── objects
│   ├── destructuring
│   └── spread/rest
│
├── Modules
│   ├── named export/import
│   └── default export/import
│
├── Async JavaScript
│   ├── Promise
│   ├── then/catch
│   ├── async/await
│   ├── fetch
│   └── error handling
│
└── Core Concepts
    ├── scope
    ├── closures
    ├── reference vs value
    ├── this
    └── event loop

TYPESCRIPT
│
├── Basic Types
│   ├── type annotations
│   └── inference
│
├── Object Modeling
│   ├── interface
│   ├── type
│   └── optional properties
│
├── Type Composition
│   ├── unions
│   └── function types
│
├── Type Safety
│   ├── narrowing
│   └── generics
│
└── Application Types
    └── API response types
```

------------------------------------------------------------------------

## Next Phase

**Phase 1 --- React + TypeScript**

Start with:

1.  What React actually is
2.  Vite project setup
3.  JSX
4.  Components
5.  Props
6.  State
7.  Events
8.  Conditional rendering
9.  Lists
10. Forms
11. `useState`
12. `useEffect`
13. API calls
14. Component communication
15. Project structure

The goal is to move from **language fundamentals → building React
applications from scratch**, using Copilot as an accelerator rather than
as the source of understanding.
