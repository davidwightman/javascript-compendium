## Functions

technically functions are objects but typeof will return function

function declaration vs function expression
HOISTING!
var hoists up variable declaration but not assignment.
let and const are not hoisted.
function declarations are hoisted but not function expressions

### function declaration

```
function name() {
    name
}
```

### function expression

```
const square = function (num) {
    return num * num
}
square(7) //49
```

### anonymous function

- the function inside the below forEach is an anonymous function because we never have to call it by name

```
[1.2,3].forEach(function(value) {
    console.log(value)
})
```

difference between arguments (the value you acually pass in) and parameters (the placeholder for what you pass in a function)

### Higher Order function

- operate on or with other functions
- accepts or returns a function

### Callback Function

A callback function is a function passed into another function as an argument, which is then invoked inside the outer function.
example: setTimeout(func, time)

### First Class Function

when a function can be treated as variables - a function can be returned as a function, passed as an argument or assigned as a value to a variable
