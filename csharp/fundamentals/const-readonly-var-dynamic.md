# 4. const, readonly, var & dynamic

## const

**Definition:** A `const` value is a compile-time constant and must be known at compile time.

```csharp
const double Pi = 3.14159;
```

**Memory hook:**

> `const` = known before the program runs.

---

## readonly

**Definition:** A `readonly` field can be assigned at declaration or in a constructor and then cannot be reassigned.

```csharp
class Employee
{
    private readonly string id;

    public Employee(string id)
    {
        this.id = id;
    }
}
```

**Memory hook:**

> `readonly` = fixed after object initialization.

---

## var

**Definition:** `var` uses compile-time type inference.

```csharp
var name = "Sunny";
```

The compiler treats this as:

```csharp
string name = "Sunny";
```

**Important:** `var` is still strongly typed.

```csharp
var name = "Sunny";

// name = 100; // compile-time error
```

**Memory hook:**

> `var` = compiler knows the type.

---

## dynamic

**Definition:** `dynamic` tells the compiler to defer member binding/type checking for that variable to runtime.

```csharp
dynamic value = "Sunny";

value.ToUpper();            // works
value.NonExistingMethod();  // compiles, fails at runtime
```

**Why use it?**

It can be useful when dealing with genuinely dynamic data or APIs whose shape isn't known at compile time.

**Trade-off:**

You lose compile-time safety.

**Memory hook:**

> `dynamic` = binding is deferred to runtime.

### var vs dynamic

```text
var
 ↓
Compiler knows type
 ↓
Compile-time checking


dynamic
 ↓
Runtime binding
 ↓
Potential runtime failure
```

---
