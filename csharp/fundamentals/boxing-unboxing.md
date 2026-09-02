# Boxing & Unboxing

## ⚡ Quick Revision
**Mental model:** Value type → object = boxing. Object containing value → value type = unboxing.

## 🧠 Understanding
Boxing creates an object representation containing a value-type value. This can involve allocation and copying.

```csharp
int x = 10;
object obj = x; // boxing
int y = (int)obj; // unboxing
```

Unboxing requires the compatible value type. Boxing can add allocation and GC pressure, which is why generics often avoid it.

## 🎤 Interview Answer
> "Boxing converts a value type into an object representation, which can require an allocation and copy. Unboxing extracts the value type from that boxed object and requires a compatible type."

## 🔄 Likely Follow-ups
- **Why can boxing hurt performance?** It may allocate and create GC pressure.
- **How do generics help?** Type-safe generic collections can avoid boxing value types.
