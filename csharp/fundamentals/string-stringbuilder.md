# 6. string & StringBuilder

## string

**Definition:** `string` is a reference type whose instances are immutable.

Immutable means:

> Once a string object exists, its contents cannot be changed.

```csharp
string name = "Sunny";

name += " Bhargav";
```

The original string is not modified. A new string is produced.

**Why it matters:**

Repeated modifications can create many string allocations.

**Memory hook:**

> `string` = immutable text.

---

## StringBuilder

**Definition:** `StringBuilder` is a mutable text-building type that maintains an internal buffer and can grow it as needed.

```csharp
var sb = new StringBuilder();

sb.Append("Hello");
sb.Append(" ");
sb.Append("Sunny");

string result = sb.ToString();
```

**Use when:**

- many repeated modifications
- loops
- building large text
- generating long documents/queries/output

**Don't use it automatically.**

For a few concatenations:

```csharp
string fullName = firstName + " " + lastName;
```

is perfectly fine.

**Memory hook:**

> Many edits → StringBuilder  
> Few edits → normal string is usually fine

---
