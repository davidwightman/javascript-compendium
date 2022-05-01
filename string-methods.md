## String Methods

Note:
strings are immutable in that you cannot change individual indexes of strings like you can with arrays. Also, even though strings have built in properties they are not objects!

### toUpperCase()

makes entire string uppercase

### toLowerCase()

makes entire string lowercase

### trim() trimStart() trimEnd()

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

### substr()

1st param what index to start, 2nd param how many characters to include

```
let str = 'abcd'
console.log(str.substr(1,2)) // 'bc'
```

### replace()

takes what you want to replace with new value. but only replaces the first found value. if it does not find it then it does nothing.

### includes()

returns boolean if string is included

```
const sentence = 'The quick brown fox jumps over the lazy dog.';

const word = 'fox';

console.log(`The word "${word}" ${sentence.includes(word) ? 'is' : 'is not'} in the sentence`);
// expected output: "The word "fox" is in the sentence"
```

### startsWith() and endsWith()

returns boolean

```
const str1 = 'Saturday night plans';

console.log(str1.startsWith('Sat'));
// expected output: true

console.log(str1.startsWith('Sat', 3));
// expected output: false

```

### split()

```
const str = 'The quick brown fox jumps over the lazy dog.';

const words = str.split(' ');
console.log(words[3]);
// expected output: "fox"

const chars = str.split('');
console.log(chars[8]);
// expected output: "k"

const strCopy = str.split();
console.log(strCopy);
// expected output: Array ["The quick brown fox jumps over the lazy dog."]
```
