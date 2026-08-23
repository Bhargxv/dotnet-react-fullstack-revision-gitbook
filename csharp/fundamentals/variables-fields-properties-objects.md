# 2. Variables, Fields, Properties & Objects

## Class vs Object

**Definition:** A class defines the structure and behavior of a type; an object is a runtime instance of that class.

```csharp
class Employee
{
    public string Name { get; set; }
}

Employee e = new Employee();
```

- `Employee` class → definition
- `e` → variable
- `new Employee()` → object

---

## Field

**Definition:** A field is a variable declared inside a class or struct to store state.

```csharp
private int age;
```

**Why it matters:** Fields represent internal data/state of an object.

**Memory hook:**

> Field = storage directly belonging to the type/object.

---

## Property

**Definition:** A property provides controlled access to a value, usually through `get` and `set` accessors.

```csharp
public int Age { get; private set; }
```

**Why it matters:** Properties are the normal C# way to expose object state while retaining control over access.

**Memory hook:**

> Field stores; property controls access.

### Auto-property

```csharp
public int Age { get; set; }
```

The compiler provides a hidden backing field.

If the property belongs to a heap object, that backing field is part of that object.

---
