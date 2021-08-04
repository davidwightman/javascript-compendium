## Types


### primitive values

You can't change primitive values, all primitive values are immutable. (variables may change, variable point to values)

number - used for math calculations
string - used for text
boolean - used for logical operators
null - used for intentioanlly missing values
- must be assigned
- typeof null is "object" (which is a lie. null is a primitve value and does not behave in any way like an object)
undefined - used for unintentionally missing values
```
console.log(typeof(undefined)); // "undefined"
```

Symbol - (uncommon) used to perform rituals and hide secrets
BigInt - (uncommon) used for math on big numbers

### reference types 

functions - used to refer to code
objects - used to group related data and code
arrays - a type of object

they point to value.

```
let example = [5,4, 3]
let example2 = example

example2.pop()
console.log(example)
// would return [5, 4]
```