# 3. Parameter Passing

## Default Parameter Passing

**Definition:** C# passes parameters by value by default.

The important question is:

> What is being copied?

### Value type

```csharp
void Update(int x)
{
    x = 50;
}

int a = 10;
Update(a);

// a is still 10
```

The value was copied.

### Reference type

```csharp
void Update(Person p)
{
    p.Age = 50;
}

Person p1 = new Person();
p1.Age = 20;

Update(p1);

// p1.Age is now 50
```

Here, the **reference was copied**, not the object.

Both variables point to the same object.

```text
Caller:
p1 ─────────────┐
                ↓
              Person
              Age = 50
                ↑
Method:
p  ─────────────┘
```

### Critical distinction

```csharp
void Update(Person p)
{
    p.Age = 50;       // object mutation
    p = new Person(); // parameter reassignment
}
```

- `p.Age = 50` changes the shared object.
- `p = new Person()` changes only the local parameter variable.

**Interview definition:**

> A method parameter of a reference type is a local variable containing a copy of the caller's reference.

---

## ref

**Definition:** `ref` passes the caller's variable by reference, allowing the method to read and replace the caller's variable itself.

```csharp
void Reset(ref Person p)
{
    p = new Person();
}

Person person = new Person();

Reset(ref person);
```

**Memory hook:**

> `ref` = method gets an alias to the caller's variable.

---

## out

**Definition:** `out` passes a variable by reference and requires the called method to assign it before returning.

Classic example:

```csharp
if (int.TryParse("123", out int value))
{
    Console.WriteLine(value);
}
```

**Memory hook:**

> `out` = "I promise to produce a value."

---

## in

**Definition:** `in` passes an argument by reference but prevents the method from modifying it through that parameter.

**Why use it?**

It can avoid copying large value types while keeping read-only semantics.

**Memory hook:**

> `in` = reference, but read-only.

---
