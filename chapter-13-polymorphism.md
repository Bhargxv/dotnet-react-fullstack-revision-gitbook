# 13. Polymorphism

**Definition:**

> Polymorphism allows the same interface or method call to produce different behavior depending on the actual runtime object.

Example:

```csharp
class ServiceRequest
{
    public virtual void CalculatePrice()
    {
        Console.WriteLine("Base pricing");
    }
}

class FTLServiceRequest : ServiceRequest
{
    public override void CalculatePrice()
    {
        Console.WriteLine("FTL pricing");
    }
}

ServiceRequest request = new FTLServiceRequest();

request.CalculatePrice();
```

Output:

```text
FTL pricing
```

Why?

```text
Variable/reference type
        ↓
ServiceRequest

Actual runtime object
        ↓
FTLServiceRequest
```

Runtime dispatch chooses the overridden implementation.

**Memory hook:**

> Same call, different behavior.

---
