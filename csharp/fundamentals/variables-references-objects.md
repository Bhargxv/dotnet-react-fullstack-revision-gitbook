# Variables, References & Objects

## ⚡ Quick Revision
**Mental model:** Type = category. Variable = named holder. Object = runtime instance. Reference = value identifying a reference-type object.

## 🧠 Understanding
```csharp
Person p = new Person();
```
`Person` is the type, `p` is the variable, and `new Person()` creates the object. For a reference type, `p` contains a reference to that object.

## 🎤 Interview Answer
> "A variable is a named storage location used by the program. An object is a runtime instance created from a type. For a reference type, the variable holds a reference to that object rather than containing the whole object directly."

## 🔄 Likely Follow-ups
- **Can two variables reference one object?** Yes.
- **What does reassignment do?** It changes one variable's reference; it doesn't reassign other variables.
