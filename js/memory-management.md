## Garbage collection

- Is an object still needed?

### References

#### Reference-counting garbage collection

> Unused by modern JS engines.

- Does an object still have other objects referencing it?
- An object references another when the former has access to the latter. Eg: an object has access to its prototype and its properties values.
- 2 objects that circularly refer to each other cannot be marked for garbage collection. Hence, this is a common cause of memory leaks.  
  eg:

```
const x = {};
const y = {};
x.a = y; // x references y
y.a = x; // y references x
```

### Mark and sweep algo

> Used by all modern JS engines.

- Is an object unreachable?
- Root: global object.
- Starting from the root, the garbage collector finds all the objects that are referenced from the root, then all objects referenced from these, and so on. Thus, it can determine the reachable and non-reachable objects.
