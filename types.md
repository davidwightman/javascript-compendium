## Types


### primitive types

number
string
boolean
null - intentioanl absence of any value
- must be assined
- typeof null is "object"
undefined - variables that do not have an assigned value

Symbol
BigInt

### reference types 

functions
objects 
arrays

they point to value.

```
let example = [5,4, 3]
let example2 = example

example2.pop()
console.log(example)
// would return [5, 4]
```