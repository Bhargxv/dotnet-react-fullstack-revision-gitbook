# `const` vs `readonly` vs `var` vs `dynamic`

## ⚡ Quick Revision
| Feature | Mental model |
|---|---|
| `const` | fixed compile-time value |
| `readonly` | fixed after initialization |
| `var` | compiler infers static type |
| `dynamic` | runtime binding |

## 🧠 Understanding
These solve different problems:
- **const:** Is this a compile-time constant?
- **readonly:** Can this field be reassigned after initialization?
- **var:** Can the compiler infer this local variable's type?
- **dynamic:** Should certain binding decisions be deferred to runtime?

## 🎤 Interview Answer
> "`const` is for compile-time constants, `readonly` is for state fixed after initialization, `var` is compile-time type inference, and `dynamic` defers binding to runtime. `var` does not remove static typing, while `dynamic` reduces compile-time checking."

## 🔄 Likely Follow-ups
- **Which is safer by default?** Prefer static typing; use `dynamic` only when runtime-dynamic behavior is genuinely needed.
