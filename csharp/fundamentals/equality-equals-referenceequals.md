# Equality: `==`, `Equals`, `ReferenceEquals`

## ⚡ Quick Revision
**Mental model:** `==` = operator-defined equality. `Equals` = equality method. `ReferenceEquals` = same object instance.

## 🧠 Understanding
`==` depends on the type/operator overload. `Equals` can be overridden to define value equality. `ReferenceEquals` specifically asks whether two references identify the same object instance.

```csharp
Person p1 = new Person { Name = "A" };
Person p2 = new Person { Name = "A" };

p1 == p2;                 // false for a plain class
p1.Equals(p2);            // false unless equality is overridden
ReferenceEquals(p1, p2);  // false
```

`string` is an important exception because it defines content-based equality for `==` and `Equals`.

## 🎤 Interview Answer
> "I don't treat these as synonyms. `==` uses the type's operator semantics, `Equals` is an equality method that can be overridden, and `ReferenceEquals` checks whether two references point to the exact same object instance."

## 🔄 Likely Follow-ups
- **Why does string `==` compare content?** `string` overloads the operator.
- **How do value objects compare?** They can override equality or use appropriate value-based equality implementations.
