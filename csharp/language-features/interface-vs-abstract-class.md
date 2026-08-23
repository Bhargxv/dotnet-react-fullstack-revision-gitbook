# 15. Interface vs Abstract Class

## Interface

**Definition:**

> An interface defines a contract or capability that implementing classes agree to provide.

Example:

```csharp
public interface IDocumentProcessor
{
    void Process();
}
```

Possible implementations:

```csharp
class ClassificationProcessor : IDocumentProcessor
{
    public void Process()
    {
    }
}

class ExtractionProcessor : IDocumentProcessor
{
    public void Process()
    {
    }
}
```

**Use interface when:**

- classes need to share a contract
- they don't necessarily share state
- they don't necessarily share implementation
- you want multiple capabilities/contracts

A class can implement multiple interfaces.

**Memory hook:**

> Interface = contract/capability.

---

## Abstract Class

**Definition:**

> An abstract class is a non-instantiable base class that can provide common state, implemented behavior, and abstract members for derived classes to implement.

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

**Use abstract class when:**

- classes form a meaningful family
- they share state
- they share implementation
- some behavior should be inherited

**Memory hook:**

> Abstract class = shared family + reusable base behavior.

### Modern C# nuance

Interfaces can have default implementations in modern C#.

So don't say:

> "Interfaces can never contain implementation."

Better:

> Interfaces primarily model contracts/capabilities, while abstract classes model a shared base/family with possible state and implementation.

---
