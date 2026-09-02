# Type System

## ⚡ Quick Revision
**Mental model:** Type = what a value is allowed to be and do.

## 🧠 Understanding
A type tells the compiler what kind of value exists and which operations are valid. Strong typing catches many invalid operations before runtime.

```csharp
int age = 25;
string name = "Sunny";
// age = name; // compile-time error
```

**Problem solved:** reliable compile-time validation of operations, conversions, members and overloads.

## 🎤 Interview Answer
> "A type defines what kind of value we're working with and what operations are valid. C# is strongly typed, so the compiler can catch many invalid operations before the application runs."

## 🔄 Likely Follow-ups
- **Is `var` dynamic?** No; its type is inferred at compile time.
- **What is `dynamic`?** Certain binding decisions are deferred to runtime.
