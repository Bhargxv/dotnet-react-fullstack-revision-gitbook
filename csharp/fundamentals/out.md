# `out`

## ⚡ Quick Revision
**Mental model:** `out` = produce mine.

## 🧠 Understanding
The method writes a value into a caller variable. The caller doesn't initialize it; the method must assign it before returning.

```csharp
if (int.TryParse("123", out int value)) { }
```

**Problem solved:** returning an additional result alongside a primary return value.

## 🎤 Interview Answer
> "`out` is used when the method is responsible for producing a value for the caller. Unlike `ref`, the caller doesn't have to initialize it because the compiler requires the method to assign it before returning."

## 🔄 Likely Follow-ups
- **Classic example?** `TryParse`.
