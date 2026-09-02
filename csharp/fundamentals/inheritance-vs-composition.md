# Inheritance vs Composition

## ⚡ Quick Revision
**Decision rule:** IS-A → consider inheritance. HAS-A → consider composition.

## 🧠 Understanding
Inheritance fits genuine families with shared behavior/state. Composition fits behavior assembled from independent collaborators. Prefer composition when inheritance would mainly be used to reuse code without a strong conceptual relationship.

## 🎤 Interview Answer
> "I choose inheritance when there is a genuine IS-A relationship and shared base behavior makes sense. I choose composition when a class needs capabilities from other objects and I want those collaborators to remain replaceable and independently testable."

## 🔄 Likely Follow-ups
- **Which is usually more flexible?** Composition, because collaborators can be replaced without changing the class hierarchy.
