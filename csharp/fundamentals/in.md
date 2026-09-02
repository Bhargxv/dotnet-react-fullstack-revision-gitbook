# `in`

## ⚡ Quick Revision
**Mental model:** `in` = look at mine, don't change it.

## 🧠 Understanding
`in` provides read-only by-reference access. It can avoid copying larger value types while preserving read-only semantics.

```csharp
void Print(in LargeStruct value) { }
```

## 🎤 Interview Answer
> "`in` passes an argument by reference but exposes it as read-only to the method. It's mainly useful when avoiding copies of larger value types matters while keeping read-only semantics."

## 🔄 Likely Follow-ups
- **`ref` / `out` / `in`?** Change an existing value / produce a value / read by reference without modifying it.
