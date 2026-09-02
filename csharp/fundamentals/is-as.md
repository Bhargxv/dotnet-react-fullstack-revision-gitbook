# `is` vs `as`

## ⚡ Quick Revision
**Mental model:** `is` = check compatibility/pattern. `as` = attempt compatible reference/nullable conversion, otherwise null.

## 🧠 Understanding
Use `is` when you need to test a type and possibly pattern-match it.

```csharp
if (obj is Person p)
    Console.WriteLine(p.Name);
```

Use `as` when a compatible reference/nullable conversion is appropriate and failure should produce `null`.

```csharp
Person p = obj as Person;
```

`as` doesn't work with non-nullable value types such as `int`, `double`, and `bool`.

## 🎤 Interview Answer
> "`is` checks type compatibility and can perform pattern matching. `as` attempts a compatible reference or nullable conversion and returns null if it can't convert."

## 🔄 Likely Follow-ups
- **Which should I prefer?** Pattern matching with `is` is often clearer when you need both the check and the converted value.
