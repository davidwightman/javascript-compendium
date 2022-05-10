## Scope

the location where a variable is defined dictates where we have access to that variable

The accessibility of variables, functions and objects in a part of your code

call

apply

bind

### block scope

- the behavior of a variable that is only accessible inside of the block it was defined. most of the time that means the nearest curly brackets.

- let and const (like let but cannot be reassigned) are block-scoped and cannot be accessed before initialization. const values can still be mutated (like with an array or object)

### function scope

- variable is accessed anywhere inside of the function it was defined

- var is function-scoped and is automatically initialized to undefined when it is hoisted.

```
console.log('varNum', varNum)
console.log('letNum', letNum)

var varNum = 0
let letNum = 0
```

the above example returns:
varNum undefined
then throws an error: Cannot access 'letNum' before initialization

### hoisting

the process oby which javascript engine moves variable declarations to the top of their scope
