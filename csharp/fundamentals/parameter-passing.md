# Parameter Passing

## ⚡ Quick Revision
**Mental model:** C# passes parameters by value by default. Ask: **what is being copied?**

| Form | Mental model | Caller initializes? | Method can modify caller variable? |
|---|---|---:|---:|
| Default | copy it | Yes | No |
| `ref` | change mine | Yes | Yes |
| `out` | produce mine | No | Yes |
| `in` | look at mine | Yes | No |

## 🧠 Understanding
For a value type, the value is copied. For a reference type, the reference is copied, so the method parameter and caller variable can refer to the same object.

```csharp
void Update(Person p)
{
    p.Age = 50;       // mutation: caller sees it
    p = new Person(); // reassignment: caller reference unchanged
}
```

This distinction is the root of many interview traps.

### `ref`
`ref` gives the method an alias to the caller's variable itself.

```csharp
void Change(ref int x) => x = 20;
int a = 10;
Change(ref a); // a == 20
```

The caller must initialize the variable before passing it.

### `out`
`out` is used when the method is responsible for producing a value. The caller doesn't initialize it; the method must assign it before returning.

```csharp
if (int.TryParse("123", out int value)) { }
```

### `in`
`in` provides read-only by-reference access. It can avoid copying larger value types while preserving read-only semantics.

```csharp
void Print(in LargeStruct value) { }
```

## 🎤 Interview Answer
> "C# passes parameters by value by default. For value types, the value is copied. For reference types, the reference is copied, not the object, so the method can mutate the shared object but reassigning its local parameter doesn't reassign the caller's variable. `ref` lets us work with the caller's variable, `out` lets the method produce a value, and `in` provides read-only by-reference access."

## 🔄 Likely Follow-ups
- **Is a reference type passed by reference by default?** No.
- **`ref` vs `out`?** `ref` requires an existing value; `out` is for producing a value.
- **Why use `in`?** Mainly to avoid copying larger value types while keeping the argument read-only.
