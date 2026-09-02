# string vs StringBuilder

## ⚡ Quick Revision
**Mental model:** `string` is immutable; `StringBuilder` is designed for repeated mutation.

## 🧠 Understanding
A string operation that appears to modify a string creates another string because strings are immutable.

```csharp
string s = "Hello";
s += " World";
```

For many repeated modifications, `StringBuilder` can reuse its internal buffer and reduce intermediate string allocations.

```csharp
var sb = new StringBuilder();
sb.Append("Hello").Append(" World");
```

## 🎤 Interview Answer
> "`string` is immutable, so operations that change its contents create new string values. `StringBuilder` is useful when I need many repeated modifications because it can build the result using a mutable buffer and reduce intermediate allocations."

## 🔄 Likely Follow-ups
- **Does every concatenation require StringBuilder?** No. Simple or compiler-optimized concatenation is often perfectly fine.
- **Why is string immutable?** It supports safe sharing, predictable behavior and string interning.
