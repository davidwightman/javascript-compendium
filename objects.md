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

### more

Set and Map classes

### checking if an object has a specific key

```
console.log('name' in website) // true but also checks on objects that it is inheriting from. so toString would be true as well
console.log(website.hasOwnProperty('name'))
```

- so use hasOwnProperty most of the time

### get

### set

### **proto**

- how to set inherited object

### iterating over an object

- Object.keys(obj) - excludes inherited keys. excludes Symbols.
- Object.values(obj)
- Object.values(obj) // [['key', 'value]]

```
for (key in obj) {
  console.log(key)
}
```

- will ignore Symbols but will include inherited properties
