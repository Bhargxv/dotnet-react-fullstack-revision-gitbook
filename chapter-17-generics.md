# 17. Generics

## What are Generics?

**Definition:**

> Generics allow reusable classes, methods, interfaces, and collections to work with different data types while maintaining compile-time type safety.

**Main benefits:**

1. Code reuse
2. Compile-time type safety
3. Less casting
4. Can avoid unnecessary boxing for value types

**Memory hook:**

> Generics = Reusability + Type Safety + Performance

---

## Generic Method

```csharp
public void Print<T>(T value)
{
    Console.WriteLine(value);
}
```

Usage:

```csharp
Print(10);
Print("Sunny");
Print(new Person());
```

`T` is a type parameter.

The actual type is determined when the method is used.

---

## Generic Collections

```csharp
List<int> numbers = new List<int>();

numbers.Add(10);

// numbers.Add("Sunny"); // compile-time error
```

The compiler knows:

```text
List<int>
   ↓
Only int values
```

---

## Why List<object> can still involve boxing

Consider:

```csharp
List<object> values = new List<object>();

values.Add(10);
values.Add("Sunny");
```

`List<T>` is generic.

But here:

```text
T = object
```

So adding:

```csharp
10
```

requires:

```text
int
 ↓
object
 ↓
boxing
```

Compare:

```csharp
List<int> values = new List<int>();

values.Add(10);
```

Here:

```text
T = int
```

The collection is specifically for `int`, so there is no need to box the integer just to store it.

**Interview answer:**

> Generics themselves do not automatically eliminate boxing. It depends on the chosen type parameter. `List<object>` can still box value types because `T` is `object`; `List<int>` stores ints directly as ints.

---

## Generic Class

```csharp
class ApiResponse<T>
{
    public bool Success { get; set; }
    public T Data { get; set; }
}
```

Usage:

```csharp
ApiResponse<Customer> response =
    new ApiResponse<Customer>();

ApiResponse<List<Customer>> listResponse =
    new ApiResponse<List<Customer>>();
```

**Mental model:**

> Write the structure once; choose the type later.

---

## Generic Constraints

**Definition:**

> Generic constraints restrict which types can be used as a type parameter.

Example:

```csharp
class Repository<T> where T : Entity
{
    public void Save(T entity)
    {
        // Can safely use members guaranteed by Entity
    }
}
```

Here:

```text
T must be Entity or derived from Entity
```

Common constraints:

```csharp
where T : class
```

T must be a reference type.

```csharp
where T : struct
```

T must be a non-nullable value type.

```csharp
where T : new()
```

T must have a public parameterless constructor.

```csharp
where T : Entity
```

T must derive from `Entity`.

```csharp
where T : IInterface
```

T must implement the interface.

**Memory hook:**

> Constraint = promise about T.

---
