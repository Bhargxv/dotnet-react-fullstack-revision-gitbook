# Inheritance

## ⚡ Quick Revision
**Mental model:** Inheritance = IS-A; a derived type reuses or extends a base type.

## 🧠 Understanding
Inheritance models a genuine family relationship and allows shared behavior/state.

```csharp
class Animal { public void Eat() {} }
class Dog : Animal { public void Bark() {} }
```

Use it when the derived type is genuinely a specialized form of the base type. A downside is coupling to the base abstraction.

## 🎤 Interview Answer
> "Inheritance lets a derived class reuse and extend behavior or state from a base class. I use it when there is a genuine IS-A relationship and the shared abstraction makes the design clearer."

## 🔄 Likely Follow-ups
- **Main risk?** Tight coupling to the base hierarchy.
- **Alternative?** Composition when behavior should be assembled rather than inherited.
