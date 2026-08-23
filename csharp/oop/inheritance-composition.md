# 12. Inheritance & Composition

## Inheritance

**Definition:**

> Inheritance allows a derived class to acquire and extend members/behavior from a base class and represents an IS-A relationship.

```csharp
class Vehicle
{
}

class Car : Vehicle
{
}
```

A Car **IS-A** Vehicle.

Another example:

```csharp
class ServiceRequest
{
}

class FTLServiceRequest : ServiceRequest
{
}

class LTLServiceRequest : ServiceRequest
{
}
```

**Memory hook:**

> IS-A → inheritance

### Important interview trap

Shared fields alone do not justify inheritance.

If:

```text
Customer
 ├── Name
 └── Phone

Employee
 ├── Name
 └── Phone
```

that does not automatically mean:

```text
Employee : Customer
```

First validate the semantic relationship.

---

## Composition

**Definition:**

> Composition models a HAS-A relationship by making one object contain or depend on another object.

Example:

```text
Vehicle
  │
  └── HAS-A → Engine
```

or:

```text
ServiceRequest
  │
  └── HAS-A → Customer
```

**Memory hook:**

> HAS-A → composition

---
