### Rest

Collects things into a single array

arguments cannot be used in arrow function but rest can

### Destructuring

1. destructuring arrays, items into their own variables. use extra comas to skip items

```
const results = [1, 2, 3, 4]

// ordered list of variable names
const [one, two, three, four] = results;
console.log(one) // returns 1
```

2. destructuring objects, into stand alone variables. in object we base variable of name of property. use colon to change names

```
const guy = {
    first: 'david',
    last: 'wightman',
    country: 'here'
}

const {first, last, country: nation} = guy
console.log(first, nation) // returns david here
```

3. use when passing in at parameter

```
function print({first, last, country}) {
    console.log(first)
}
// returns david
```
