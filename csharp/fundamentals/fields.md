# Fields

## ⚡ Quick Revision
**Mental model:** Field = stored state inside a type.

## 🧠 Understanding
A field is a variable declared inside a class or struct. Instance fields belong to objects; static fields belong to the type.

```csharp
class Employee { private int age; }
```

Fields are implementation storage. Public APIs usually expose state through properties or behavior instead.

## 🎤 Interview Answer
> "A field is a variable declared inside a class or struct that stores state. Instance fields belong to an object, while static fields belong to the type."

## 🔄 Likely Follow-ups
- **Field vs property?** Field is storage; property is controlled access to a value.
