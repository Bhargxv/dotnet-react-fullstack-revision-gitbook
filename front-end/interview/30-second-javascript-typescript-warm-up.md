# 35. 30-Second JavaScript & TypeScript Warm-Up

If asked:

### "What is JavaScript?"

> JavaScript is a dynamically typed programming language commonly used
> for web application behavior and also used outside the browser through
> environments such as Node.js.

### "What is TypeScript?"

> TypeScript is a superset of JavaScript that adds static type checking
> and development-time features. It is transformed into JavaScript
> before execution.

### "What is a callback?"

> A callback is a function passed to another function so that the
> receiving function can invoke it later or as part of its operation.

### "What is a Promise?"

> A Promise represents the eventual result of an asynchronous operation
> and can be pending, fulfilled or rejected.

### "What does async/await do?"

> `async` makes a function return a Promise, while `await` lets us
> consume a Promise in a sequential-looking way without blocking the
> entire JavaScript execution.

### "What is a closure?"

> A closure is a function that retains access to variables from its
> surrounding lexical scope even after the outer function has finished
> executing.

### "What is the difference between `user2 = user1` and `{ ...user1 }`?"

> Assignment copies the reference, so both variables refer to the same
> object. Spread creates a new top-level object and copies the
> properties into it.

### "What is `response` vs `response.json()`?"

> `response` is the HTTP Response object. `response.json()` reads and
> parses the response body and returns a Promise for the resulting
> JavaScript value.

### "Does fetch throw for HTTP 404?"

> No. `fetch` normally resolves with a Response object for HTTP errors
> such as 404 or 500. We should check `response.ok` and throw or
> otherwise handle the error ourselves.

------------------------------------------------------------------------
