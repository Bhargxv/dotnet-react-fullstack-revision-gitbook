# Class vs Object

## ⚡ Quick Revision
**Mental model:** Class = definition. Object = runtime instance.

## 🧠 Understanding
A class defines structure and behavior; an object is a concrete instance with runtime state.

```csharp
class Employee { public string Name { get; set; } }
Employee e = new Employee();
```

**Problem solved:** reusable type definitions plus concrete instances in the running application.

## 🎤 Interview Answer
> "A class defines the structure and behavior of a type, while an object is a runtime instance of that class. Multiple objects can be created from the same class, each with its own state."

## 🔄 Likely Follow-ups
- **Can a class have static members?** Yes; those belong to the type rather than an instance.
