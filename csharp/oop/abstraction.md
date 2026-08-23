# 11. Abstraction

**Definition:**

> Abstraction exposes what the caller needs while hiding unnecessary implementation details.

Example:

```csharp
documentService.Process(file);
```

The caller does not need to know that internally the service might use:

```text
Blob Storage
     ↓
Document Intelligence
     ↓
Classification
     ↓
Extraction
     ↓
Cosmos DB
     ↓
Messaging
```

The caller only cares about:

```text
Process(document)
      ↓
Result
```

**Memory hook:**

> Abstraction = hide complexity; show what matters.

---

## Encapsulation vs Abstraction

This is a common interview question.

### Encapsulation

> How do I protect/control the object's state?

### Abstraction

> What implementation details can I hide from the caller?

Simple memory:

```text
Encapsulation → Protect
Abstraction   → Hide
```

---
