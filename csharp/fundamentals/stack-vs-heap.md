# Stack vs Heap

## ⚡ Quick Revision
**Mental model:** Stack = method execution workspace. Heap = managed object storage.

## 🧠 Understanding
The stack is associated with call frames and local execution state. The managed heap stores objects whose lifetimes are managed by the garbage collector.

```csharp
void Process()
{
    int x = 10;
    Person p = new Person();
}
```

Use this as a runtime mental model, not as "value types = stack, reference types = heap." A value-type field can live inside a heap object.

## 🎤 Interview Answer
> "The stack is primarily associated with method call frames and local execution state, while the managed heap stores objects whose lifetimes are managed by the garbage collector. Stack/heap and value/reference are related but not interchangeable concepts."

## 🔄 Likely Follow-ups
- **Who cleans managed heap objects?** The garbage collector.
- **Does every local variable live on the stack?** Avoid that absolute simplification; focus on execution semantics rather than a simplistic placement rule.
