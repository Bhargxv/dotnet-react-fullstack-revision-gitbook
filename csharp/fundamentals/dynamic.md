# `dynamic`

## ⚡ Quick Revision
**Mental model:** `dynamic` = runtime binding.

## 🧠 Understanding
`dynamic` defers certain member binding and type checking decisions until runtime.

```csharp
dynamic value = "Sunny";
value.ToUpper();
value.NonExistingMethod(); // runtime failure
```

Use it when the runtime shape really is dynamic; the trade-off is reduced compile-time safety.

## 🎤 Interview Answer
> "`dynamic` defers certain binding decisions to runtime. It can be useful for genuinely dynamic APIs or data, but the trade-off is losing some compile-time safety and potentially discovering errors at runtime."

## 🔄 Likely Follow-ups
- **Is dynamic the same as var?** No. `var` preserves static typing; `dynamic` defers binding.
