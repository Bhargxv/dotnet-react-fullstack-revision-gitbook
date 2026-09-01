# 15. Interface vs Abstract Class

## Start with the problem

When designing classes, two different questions can come up:

1. **Do different classes simply need to promise the same capability?**
2. **Or are they genuinely part of the same family and should share state/implementation?**

Those two problems lead to two different tools: **interfaces** and **abstract classes**.

---

## Interface

### Mental model

> **Interface = WHAT I need, not HOW it is done.**

An interface is useful when a consumer needs a capability/contract but should not be tied to a particular implementation.

Imagine:

```csharp
class OrderService
{
    private SqlOrderRepository _repository = new SqlOrderRepository();
}
```

Now `OrderService` knows that persistence is specifically SQL. If we later want a different implementation—for example a NoSQL repository, cached repository, or mock for testing—`OrderService` itself has to change.

Instead:

```csharp
public interface IOrderRepository
{
    void Save(Order order);
}
```

Now `OrderService` can depend on the capability it needs:

```csharp
class OrderService
{
    private readonly IOrderRepository _repository;

    public OrderService(IOrderRepository repository)
    {
        _repository = repository;
    }
}
```

Possible implementations:

```text
IOrderRepository       <- WHAT OrderService needs
       |
       +-- SqlOrderRepository
       +-- CosmosOrderRepository
       +-- MockOrderRepository
                         ^
                         HOW it is implemented
```

### Why use an interface?

- Separate the consumer from a concrete implementation.
- Make implementations replaceable.
- Make testing easier by allowing test doubles/mocks.
- Represent a capability shared by classes that don't necessarily belong to the same inheritance family.
- Allow a class to implement multiple contracts.

### Interview answer

> **"I use an interface when the consumer needs a contract or capability but shouldn't need to know the implementation behind it. For example, an OrderService may need something that can save an order, but it shouldn't care whether that is implemented using SQL, Cosmos DB, or a mock. The interface gives us that separation and makes the implementation easier to replace and test."**

### Follow-up: interface vs dependency injection

These concepts solve different parts of the problem:

> **Interface → WHAT do I depend on?**
>
> **Dependency Injection → WHO provides the implementation?**

For example:

```csharp
builder.Services.AddScoped<IOrderRepository, SqlOrderRepository>();
```

The service depends on `IOrderRepository`; the DI container supplies the registered implementation.

---

## Abstract Class

### Start with the problem

Sometimes classes are not merely sharing a capability. They are genuinely part of the **same family**, and there is useful state or behavior that should be shared.

For example, different document processors may all have a file name and common logging behavior:

```csharp
abstract class DocumentProcessor
{
    public string FileName { get; set; }

    public void LogProcessing()
    {
        Console.WriteLine("Processing...");
    }

    public abstract void Process();
}
```

Derived classes inherit the common state/behavior and provide the parts that differ.

### Mental model

> **Abstract class = shared family + reusable base behavior/state.**

### Use an abstract class when

- The classes have a meaningful **IS-A** relationship.
- They genuinely belong to the same conceptual family.
- They need shared state.
- They need shared implementation.
- Some behavior should be inherited while other behavior remains abstract.

### Interview answer

> **"I'd use an abstract class when the classes form a meaningful family and there is common state or implementation that should be shared. The base class can provide reusable behavior while leaving some operations abstract for derived classes to implement."**

---

## Quick decision rule

Ask yourself:

> **"Do I need a capability, or do I have a shared family?"**

```text
Capability / contract only
        -> Interface

Shared family + state/implementation
        -> Abstract class
```

### Modern C# nuance

Interfaces can have default implementations in modern C#.

So don't say:

> "Interfaces can never contain implementation."

Better:

> **"Interfaces primarily model contracts/capabilities, while abstract classes model a shared base/family with possible state and implementation."**
