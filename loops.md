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

If you want to access both the key and the value, you can use Array.prototype.entries() with destructuring:

```
for (const [index, value] of [1, 2, 3, 4, 5].entries()) {
  console.log(index, value);
}
```

### for... in

Loop iterating over objects.

Example from Mozilla:

```
const object = {a: 1, b: 2, c: 3};

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}

// expected output:
// "a: 1"
// "b: 2"
// "c: 3"
```
