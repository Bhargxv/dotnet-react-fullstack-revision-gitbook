# `ref`

## ⚡ Quick Revision
**Mental model:** `ref` = change mine.

## 🧠 Understanding
`ref` gives the method an alias to the caller's variable itself.

```csharp
void Change(ref int x) => x = 20;
int a = 10;
Change(ref a); // a == 20
```

The caller must initialize the variable first.

## 🎤 Interview Answer
> "`ref` lets a method operate on the caller's variable itself instead of a copied value. The caller must initialize the variable first, and changes made through the ref parameter are visible to the caller."

## 🔄 Likely Follow-ups
- **`ref` vs `out`?** `ref` requires an existing value; `out` is for producing a value.
