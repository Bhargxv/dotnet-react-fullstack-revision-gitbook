# `const`

## ⚡ Quick Revision
**Mental model:** `const` = fixed at compile time.

## 🧠 Understanding
A constant must have a compile-time constant value and cannot be reassigned.

```csharp
const double Pi = 3.14159;
```

Use it when the value is genuinely constant by definition.

## 🎤 Interview Answer
> "`const` represents a compile-time constant. Its value must be known at compile time and cannot change."

## 🔄 Likely Follow-ups
- **Can a const be assigned in a constructor?** No.
- **Difference from readonly?** `const` is compile-time; `readonly` can be initialized at runtime and then fixed.
