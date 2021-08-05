## Objects

### Types of objects
- arrays, dates, RegExps, and other non-primitive values:
```
console.log(typeof({})); // "object"
console.log(typeof([])); // "object"
console.log(typeof(new Date())); // "object"
console.log(typeof(/\d+/)); // "object"
console.log(typeof(Math)); // "object"
```

### Shorthand object properties

```
{max: max,
min: min, 
sum: sum}
{max,
min,
sum
}
```

### computed properties

```
const team {
    [role]: person
}

// same as
const team = {}
team[role] = person
```

### method shorthand syntax

```
const math = {
    add(x,y) {
        return x + y
    },
    multiply(x,y){
        return x* y
    }
}
```

### this

the value of this depends on the invocation context of the function it is used in.

arrow function will not bind to object but the Window object of object.

