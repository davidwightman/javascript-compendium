### Rest

Condense multiple elements into a single array.

```
const arr [1,2,3,4,5,6]
const [first, second, ...rest] = arr;
console.log(rest) // [3,4,5,6]
```

Rest can also be used to accept an infinite number of arguments which are then accessible as an array

```
function myFunc(...args) {
    console.log(args) // [1,2,3,4]
    }
    console.log(myFunc([1,2,3,4]))
```

### Spread

```
const arr1 = [1,2]
const arr2 = [3,4,5]

const combinedArr = [...arr1, ...arr2] // [1,2,3,4,5]
```

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
