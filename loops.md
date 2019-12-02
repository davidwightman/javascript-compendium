## Loops
### for... of

Loop iterating over built-in String, Array, AND array-like objects (e.g., arguments or NodeList), TypedArray, Map, Set, and user-defined iterables.
Example from Mozilla:
```
const array1 = ['a', 'b', 'c'];

for (const element of array1) {
  console.log(element);
}

// expected output: "a"
// expected output: "b"
// expected output: "c"
```