# 8. is & as

## is

**Definition:** `is` checks whether an object is compatible with a type and can also perform pattern matching.

```csharp
if (obj is Person p)
{
    Console.WriteLine(p.Name);
}
```

**Memory hook:**

> `is` = "Is this compatible with that type?"

---

## as

**Definition:** `as` attempts a compatible reference/nullable conversion and returns `null` if the conversion cannot be performed.

```csharp
Person p = obj as Person;

if (p != null)
{
    Console.WriteLine(p.Name);
}
```

**Memory hook:**

> `as` = try conversion; if it fails, give null.

### Important nuance

`as` cannot be used with non-nullable value types such as:

```csharp
int
double
bool
```

For those, use pattern matching or explicit conversion where appropriate.

---
