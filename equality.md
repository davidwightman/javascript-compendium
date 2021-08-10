## Equality

- Strict Equality: a === b (triple equals)
```
// Exceptions to strict equality: 
NaN === NaN // is false, although they are the same value.
-0 === 0 and 0 === -0 // are true, although they are different values.
```
- Loose Equality: a == b (double equals).
```
console.log([[]] == ''); // true
console.log(true == [1]); // true
console.log(false == [0]); // true

if (x == null) {
  // ...
}

if (x === null || x === undefined) {
  // ...
}

```
- Same Value Equality: Object.is(a, b) // works on objects or primitive values
