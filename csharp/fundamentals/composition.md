# Composition

## ⚡ Quick Revision
**Mental model:** Composition = HAS-A; build behavior by combining objects.

## 🧠 Understanding
Instead of inheriting implementation, a class owns or receives collaborators.

```csharp
class OrderService
{
    private readonly IOrderRepository repository;
    public OrderService(IOrderRepository repository) => this.repository = repository;
}
```

Composition usually provides flexibility because collaborators can be replaced independently.

## 🎤 Interview Answer
> "Composition means building a class from collaborators rather than inheriting their implementation. It models HAS-A relationships and often reduces coupling because dependencies can be replaced independently."

## 🔄 Likely Follow-ups
- **Inheritance vs composition?** IS-A/shared family versus HAS-A/assembled behavior.
