# Value Types vs Reference Types

## ⚡ Quick Revision
**Mental model:** Value → another copy of the value. Reference → another reference to the same object.

## 🧠 Understanding
This explains copying, mutation, reassignment and parameter-passing behavior.

```csharp
int a = 10;
int b = a;
b = 20; // a remains 10

Person p1 = new Person();
Person p2 = p1;
p2.Name = "Sunny"; // p1.Name is also Sunny
```

With reference types, assignment copies the reference, not the object. Reassignment changes one variable; mutation changes the shared object.

**Important:** Don't equate value/reference types with stack/heap. Those are different concepts.

## 🎤 Interview Answer
> "With a value type, assignment normally gives me another copy. With a reference type, assignment copies the reference, so two variables can point to the same object. Mutation can therefore be visible through both variables, while reassigning one reference doesn't affect the other."

## 🔄 Likely Follow-ups
- **Are reference types passed by reference?** No. The reference is passed by value by default.
- **Mutation vs reassignment?** Mutation changes the object; reassignment changes what a variable points to.
