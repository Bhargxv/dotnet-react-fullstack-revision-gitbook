# `var`

## ⚡ Quick Revision
**Mental model:** `var` = compiler infers the type.

## 🧠 Understanding
`var` uses compile-time type inference; it does not make the variable dynamically typed.

```csharp
var name = "Sunny"; // string
// name = 100;      // compile-time error
```

## 🎤 Interview Answer
> "`var` is compile-time type inference. The compiler determines the variable's type from the initializer, so the resulting variable remains strongly typed."

## 🔄 Likely Follow-ups
- **`var` vs `dynamic`?** `var` is statically typed after inference; `dynamic` defers binding to runtime.
