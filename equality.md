## Equality

- Strict Equality: a === b (triple equals)
```
// Exceptions to strict equality: 
NaN === NaN // is false, although they are the same value.
-0 === 0 and 0 === -0 // are true, although they are different values.
```
- Loose Equality: a == b (double equals).
- Same Value Equality: Object.is(a, b) // works on objects or primitive values
