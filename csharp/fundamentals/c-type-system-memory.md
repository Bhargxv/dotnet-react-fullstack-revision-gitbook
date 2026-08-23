# 1. C# Type System & Memory

## What is a type?

**Definition:** A type defines what kind of data a value represents and what operations are valid for that data.

**Why it matters:** Types give the compiler information about values, behavior, memory representation, and allowed operations.

```csharp
int age = 25;
Person employee = new Person();
```

**Memory hook:** Type = what a value is allowed to be and do.

---

## Value Types vs Reference Types

**Definition:** Value types contain their value directly; reference-type variables contain a reference to an object.

**Why it matters:** This distinction explains copying behavior, mutation, parameter passing, and many interview questions.

**Value types:** `int`, `bool`, `struct`, `enum`

**Reference types:** `class`, `string`, arrays, `List<T>`

```csharp
int a = 10;
int b = a;
b = 20;

// a = 10
// b = 20
```

With a reference type:

```csharp
Person p1 = new Person();
Person p2 = p1;

p2.Name = "Sunny";

// p1.Name is also "Sunny"
// because both references point to the same object.
```

### Important interview correction

Do **not** say:

> "All value types are on the stack and all reference types are on the heap."

That is an oversimplification.

A value-type field can live inside a heap object. A reference-type variable can be a local variable in a method.

**Better mental model:**

> Value/reference type describes copying and representation semantics, not simply stack vs heap location.

---

## Stack vs Heap

**Definition:** The stack is used for method execution frames and local execution state; the managed heap stores objects whose lifetime is managed by the garbage collector.

**Why it matters:** It helps explain references, object lifetime, recursion, allocations, and garbage collection.

```csharp
void Method()
{
    int x = 10;
    Person p = new Person();
}
```

Think:

```text
STACK
----------------
x = 10
p = reference
----------------

HEAP
----------------
Person object
----------------
```

**Memory hook:**

> Stack = execution workspace  
> Heap = object warehouse




STACK
= Method execution
= Call frames
= Local execution state
= LIFO

HEAP
= Objects
= Dynamic allocation
= Garbage Collector
= Object lifetime





---

## Object, Variable and Reference

**Definition:** A variable is a named storage location; an object is a runtime instance; a reference is the value that identifies/points to a reference-type object.

```csharp
Person p = new Person();
```

Here:

- `Person` → type
- `p` → variable
- `new Person()` → creates object
- `p` → contains a reference to that object

**Memory hook:**

> Type = blueprint/category  
> Variable = named holder  
> Object = actual instance

---
