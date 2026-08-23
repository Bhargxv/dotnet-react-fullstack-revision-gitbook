# 19. 30-Second C# Fundamentals Warm-Up

C# is strongly typed. A type defines what values and operations are valid.

Value types copy values; reference-type variables copy references to objects.

A class defines a type, while an object is its runtime instance.

Fields store state and properties control access to state.

C# passes parameters by value by default. With reference types, the reference is copied, not the object. `ref`, `out`, and `in` provide explicit by-reference behavior.

`const` is compile-time, `readonly` is fixed after initialization, `var` is compile-time type inference, and `dynamic` defers binding to runtime.

Boxing converts a value type to an object representation and can allocate; unboxing extracts the value type.

`string` is immutable, while `StringBuilder` is mutable and useful for repeated text changes.

`==` and `Equals` depend on the type's equality semantics; `ReferenceEquals` checks object identity.

OOP has four core pillars:

- Encapsulation → protect/control state
- Abstraction → hide complexity
- Inheritance → IS-A
- Polymorphism → same call, different behavior

Overloading is compile-time; overriding is runtime.

Interfaces model contracts/capabilities. Abstract classes model shared base families.

Access modifiers control visibility.

Generics provide reusable, type-safe code and can avoid unnecessary boxing for value types.

---

# Final Memory Map

```text
C# FUNDAMENTALS
│
├── TYPE SYSTEM
│   ├── Value types
│   │   └── Copy value
│   │
│   └── Reference types
│       └── Copy reference
│
├── MEMORY
│   ├── Stack
│   │   └── Method execution/local state
│   │
│   └── Heap
│       └── Managed objects
│
├── DATA & ACCESS
│   ├── Field
│   │   └── Stores state
│   │
│   └── Property
│       └── Controls access
│
├── PARAMETER PASSING
│   ├── by value → default
│   ├── ref → caller variable alias
│   ├── out → method must produce value
│   └── in → read-only by-reference
│
├── LANGUAGE FEATURES
│   ├── const → compile-time constant
│   ├── readonly → fixed after initialization
│   ├── var → compile-time inference
│   └── dynamic → runtime binding
│
├── OBJECT HANDLING
│   ├── Boxing
│   ├── Unboxing
│   ├── string
│   ├── StringBuilder
│   ├── ==
│   ├── Equals
│   ├── ReferenceEquals
│   ├── is
│   └── as
│
├── OOP
│   ├── Encapsulation → Protect / Control
│   ├── Abstraction   → Hide complexity
│   ├── Inheritance   → IS-A
│   └── Polymorphism  → Same call, different behavior
│
└── REUSABILITY
    └── Generics
        ├── Reusability
        ├── Type Safety
        └── Less unnecessary boxing
```

---

# How to Use These Notes Before an Interview

### 15-minute warm-up

**Minutes 1–3:**  
Type system + value/reference + stack/heap

**Minutes 4–6:**  
Parameter passing + const/readonly + var/dynamic

**Minutes 7–9:**  
Boxing + string + equality

**Minutes 10–12:**  
Four OOP pillars + inheritance/polymorphism

**Minutes 13–15:**  
Interface/abstract class + access modifiers + generics

Then ask yourself:

> "Can I explain each concept without reading the answer?"

If yes, move on to deeper interview topics.
