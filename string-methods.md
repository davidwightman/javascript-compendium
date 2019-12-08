## String Methods

### toUpperCase()
makes entire string uppercase

### trim()
returns version with no spaces at the beginning or end. (leaves spaces in the middle)

### indexOf()
pass in substring and it returns the index of where the first substring found starts. returns -1 if not found. It is case sensitive.

```
var paragraph = 'The quick brown fox jumps over the lazy dog. If the dog barked, was it really lazy?';

var searchTerm = 'dog';
var indexOfFirst = paragraph.indexOf(searchTerm);

console.log('The index of the first "' + searchTerm + '" from the beginning is ' + indexOfFirst);
// expected output: "The index of the first "dog" from the beginning is 40"

console.log('The index of the 2nd "' + searchTerm + '" is ' + paragraph.indexOf(searchTerm, (indexOfFirst + 1)));
// expected output: "The index of the 2nd "dog" is 52"
```

### slice()

single number (begin index): takes slice starting from index 4 to the end 

two numbers (begin and end index): 1st number is index of where to start slice, index of where to end slice. 

### replace()

takes what you want to replace with new value. but only replaces the first found value. if it does not find it then it does nothing.