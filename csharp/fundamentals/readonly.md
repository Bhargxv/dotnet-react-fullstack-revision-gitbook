# `readonly`

## ⚡ Quick Revision
**Mental model:** `readonly` = fixed after initialization.

## 🧠 Understanding
A readonly field can be assigned at declaration or in a constructor, then cannot be reassigned.

```csharp
class Employee
{
    private readonly string id;
    public Employee(string id) => this.id = id;
}
```

Unlike `const`, different instances can have different readonly values.

## 🎤 Interview Answer
> "A readonly field can be initialized at declaration or during construction and then cannot be reassigned. Unlike const, its value doesn't need to be known at compile time."

## 🔄 Likely Follow-ups
- **Can a readonly reference point to a mutable object?** Yes; readonly prevents changing the reference, not necessarily mutating the object.
