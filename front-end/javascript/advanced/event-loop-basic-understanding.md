# 22. Event Loop --- Basic Understanding

JavaScript executes synchronous code first and uses asynchronous
mechanisms to schedule work that can continue later.

Example:

``` js
console.log("Start");

setTimeout(() => {
    console.log("Timeout");
}, 0);

console.log("End");
```

Output:

``` text
Start
End
Timeout
```

Even with `0` milliseconds, the timeout callback does not run
immediately.

It is scheduled to run after the current synchronous work has completed
and the event loop can process the callback.

**Important correction:**

> Do not say "JavaScript puts the thread on hold."

Better:

> The current synchronous code continues; the callback is scheduled to
> run later.

------------------------------------------------------------------------
