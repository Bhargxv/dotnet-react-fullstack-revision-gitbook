# 7. Equality: ==, Equals, ReferenceEquals

## ==

**Definition:** `==` is an operator whose behavior depends on the type/operator implementation.

For ordinary reference types, it normally checks reference equality unless the type overloads the operator.

`string` is an important exception because it overloads `==` for content comparison.

```csharp
string a = "Hello";
string b = "Hello";

Console.WriteLine(a == b); // true
```

**Memory hook:**

> `==` depends on the type.

---

## Equals()

**Definition:** `Equals()` is a method used for equality comparison. Types can override it to define value-based equality.

For example, `string` overrides it so equal text compares as equal.

```csharp
string a = "Hello";
string b = "Hello";

a.Equals(b); // true
```

---

## ReferenceEquals()

**Definition:** `ReferenceEquals()` checks whether two references refer to the exact same object instance.

```csharp
ReferenceEquals(p1, p2);
```

**Memory hook:**

> `ReferenceEquals` = "Are these the same object?"

### Plain class example

```csharp
class Person
{
    public string Name { get; set; }
}

Person p1 = new Person { Name = "A" };
Person p2 = new Person { Name = "A" };

p1 == p2;                 // false
p1.Equals(p2);            // false
ReferenceEquals(p1, p2);  // false
```

Why?

They contain similar data but are different objects.

---
