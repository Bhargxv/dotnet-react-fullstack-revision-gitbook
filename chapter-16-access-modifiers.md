# 16. Access Modifiers

## public

Accessible wherever the containing type/member is accessible.

```csharp
public int Age;
```

---

## private

Accessible only within the declaring type.

```csharp
private int age;
```

**Memory:**

> private = me

---

## protected

Accessible within the declaring type and derived classes.

```csharp
protected int age;
```

**Memory:**

> protected = me + children

---

## internal

Accessible within the same assembly.

**Memory:**

> internal = same assembly

---

## protected internal

Accessible from:

- same assembly
- OR derived classes in another assembly

---

## private protected

Accessible from:

- derived classes
- within the same assembly

---

## Defaults

Top-level class:

```csharp
class Employee
{
}
```

defaults to:

```csharp
internal class Employee
{
}
```

Class members default to:

```csharp
private
```

---
