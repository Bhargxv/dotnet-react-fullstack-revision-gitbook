# 5. Boxing & Unboxing

## Boxing

**Definition:** Boxing converts a value type into an object/reference representation, creating a boxed object containing the value.

```csharp
int x = 10;

object obj = x; // boxing
```

Conceptually:

```text
x
10

      boxing
        ↓

HEAP
┌──────────────┐
│ boxed int 10 │
└──────────────┘
        ↑
       obj
```

**Why it matters:**

Boxing can involve:

- heap allocation
- copying the value
- additional GC pressure

---

## Unboxing

**Definition:** Unboxing explicitly extracts the value type from a boxed object.

```csharp
int y = (int)obj;
```

The target type must match the boxed value.

```csharp
object obj = 10;

int x = (int)obj;      // correct
string s = (string)obj; // InvalidCastException
```

**Memory hook:**

> Value type → object = boxing  
> Object box → exact value type = unboxing

### Important example

```csharp
int x = 10;
object obj = x;

x = 20;

// obj still contains boxed 10
```

There are two separate values:

- original `x`
- boxed copy inside `obj`

---
