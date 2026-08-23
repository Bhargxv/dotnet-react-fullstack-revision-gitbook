# 10. Encapsulation

**Definition:**

> Encapsulation bundles related data and behavior together and controls how the object's state can be accessed or modified.

**Why it matters:**

It protects invariants and allows business rules to be enforced at the correct boundary.

Example:

```csharp
class BankAccount
{
    public decimal Balance { get; private set; }

    public void Withdraw(decimal amount)
    {
        if (amount <= 0)
            throw new ArgumentException();

        if (amount > Balance)
            throw new InvalidOperationException();

        Balance -= amount;
    }
}
```

A caller cannot simply do:

```csharp
account.Balance = -100000;
```

because the setter is private.

Instead, state changes through controlled behavior:

```csharp
account.Withdraw(500);
```

**Memory hook:**

> Encapsulation = protect/control object state.

### Important distinction

`private` is a **tool** used to achieve encapsulation.

It is not the definition of encapsulation.

---
