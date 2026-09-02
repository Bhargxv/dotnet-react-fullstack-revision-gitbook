# Properties

## ⚡ Quick Revision
**Mental model:** Property = controlled access to a value.

## 🧠 Understanding
Properties expose values through accessors and can restrict or customize reading and writing.

```csharp
public int Age { get; private set; }
```

An auto-property gets compiler-provided backing storage. Properties provide a stable public contract even if internal representation changes.

## 🎤 Interview Answer
> "A property provides controlled access to a value through get and set accessors. Compared with a field, it gives us a cleaner public contract and lets us restrict or customize access."

## 🔄 Likely Follow-ups
- **What does `private set` mean?** Other code can read it, but only the declaring type can set it.
