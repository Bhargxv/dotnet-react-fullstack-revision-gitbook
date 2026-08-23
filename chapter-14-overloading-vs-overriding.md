# 14. Overloading vs Overriding

## Method Overloading

**Definition:**

> Multiple methods have the same name but different parameter lists.

```csharp
Add(int a, int b)

Add(int a, int b, int c)

Add(double a, double b)
```

**Resolution:** Compile time.

**Memory hook:**

> Overloading = same name, different signature, compile time.

### Important rule

You cannot overload methods solely by changing the return type.

This is invalid:

```csharp
int Add(int a, int b)
double Add(int a, int b)
```

---

## Method Overriding

**Definition:**

> A derived class provides a new implementation of a base class virtual or abstract member.

```csharp
class Animal
{
    public virtual void Speak()
    {
        Console.WriteLine("Animal sound");
    }
}

class Dog : Animal
{
    public override void Speak()
    {
        Console.WriteLine("Bark");
    }
}
```

**Resolution:** Runtime.

**Memory hook:**

> Overriding = derived implementation, runtime dispatch.

### Interview answer

> Overloading is resolved at compile time based on the method signature/arguments; overriding is resolved at runtime based on the actual object type.

---
