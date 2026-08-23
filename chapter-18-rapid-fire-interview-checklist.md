# 18. Rapid-Fire Interview Checklist

Use these to test yourself without looking at the answers.

### Type System

**What is a type?**  
A definition of what values and operations are valid for a kind of data.

**Value vs reference type?**  
Value types copy values; reference-type assignment copies references.

**Are all value types on the stack?**  
No. Location depends on context.

**What is a reference?**  
A value that identifies/points to a reference-type object.

**Class vs object?**  
Class defines the type; object is a runtime instance.

**Field vs property?**  
Field stores state; property provides controlled access to state.

### Parameters

**How are parameters passed by default?**  
By value.

**What happens with a reference-type parameter?**  
The reference is copied, so both variables can point to the same object.

**ref vs out?**  
`ref` can read/write the caller variable; `out` must assign a value before returning.

**What is in?**  
Read-only by-reference parameter.

### Language Features

**const vs readonly?**  
`const` is compile-time; `readonly` becomes fixed after initialization/constructor.

**var vs dynamic?**  
`var` is compile-time inferred; `dynamic` defers binding to runtime.

**What is boxing?**  
Converting a value type into an object representation, typically involving a boxed heap object.

**Why is boxing expensive?**  
It can involve allocation, copying, and GC pressure.

### Strings

**Why is string immutable?**  
A string instance cannot be modified; operations that appear to modify it produce another string.

**When use StringBuilder?**  
Many repeated text modifications, especially loops or large text construction.

### Equality

**== vs Equals?**  
`==` is an operator whose behavior depends on the type; `Equals` is an equality method that types can override.

**ReferenceEquals?**  
Checks whether two references refer to the same object instance.

### Type Checking

**is vs as?**  
`is` checks compatibility/pattern matches; `as` attempts compatible conversion and returns null on failure.

### OOP

**Four OOP pillars?**

- Encapsulation
- Abstraction
- Inheritance
- Polymorphism

**Encapsulation?**  
Protect/control object state.

**Abstraction?**  
Hide unnecessary implementation complexity.

**Inheritance?**  
IS-A relationship and specialization.

**Composition?**  
HAS-A relationship.

**Polymorphism?**  
Same contract/call, different behavior.

**Overloading vs overriding?**  
Overloading = compile time. Overriding = runtime.

**Interface vs abstract class?**  
Interface primarily models a contract/capability; abstract class models a shared base/family with possible state and implementation.

### Access Modifiers

**private?**  
Declaring type only.

**protected?**  
Declaring type + derived types.

**internal?**  
Same assembly.

**public?**  
Broadly accessible wherever the containing type/member is accessible.

### Generics

**Why generics?**  
Reusable code + compile-time type safety + less casting + potentially less boxing.

**Why can List<object> box an int?**  
Because T is object, so the int value must be converted to object.

**What are generic constraints?**  
Rules restricting which types can be used for T.

---
