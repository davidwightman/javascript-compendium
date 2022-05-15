## Array Methods

array literal syntax
let arr = []

the other way to create an array:

let arr = new Array('david')

### push - array method

Adds one or more elements to the end of array and returns the new length of the array

Example from Mozilla:

```
const animals = ['pigs', 'goats', 'sheep'];

const count = animals.push('cows');
console.log(count);
// expected output: 4
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows"]

animals.push('chickens', 'cats', 'dogs');
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows", "chickens", "cats", "dogs"]

```

### pop - array method

remove from end and returns it to you

### shift - array method

removes the first element of an array and returns that element

### unshift - array method

adds one or more elements to the beginning of an array and returns the new length of the array

```
const array1 = [1, 2, 3];

console.log(array1.unshift(4, 5));
// expected output: 5

console.log(array1);
// expected output: Array [4, 5, 1, 2, 3]
```

### concat - array method

used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

```
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];

console.log(array1.concat(array2));
// expected output: Array ["a", "b", "c", "d", "e", "f"]
```

### includes - array method

determines whether an array includes a certain value among its entries, returning true or false as appropriate

```
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// expected output: true

console.log(pets.includes('at'));
// expected output: false
```

### indexOf - array method

returns the first index at which a given element can be fount in the array, or -1 if it is not present.

Example from Mozilla:

```
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// expected output: 1

// start from index 2
console.log(beasts.indexOf('bison', 2));
// expected output: 4

console.log(beasts.indexOf('giraffe'));
// expected output: -1
```

### reverse - array method

reverses an array in place. the first array element becomes the last, and last becomes first. mutates the original array.

### join - array method

creates and returns a new string by concatenating all of the elements in an array (or an array-like-object), seperated by commas or a specified seperator string. if the array has only one item, the that item will be returned without using the seperator

```
const elements = ['Fire', 'Air', 'Water'];

console.log(elements.join());
// expected output: "Fire,Air,Water"

console.log(elements.join(''));
// expected output: "FireAirWater"

console.log(elements.join('-'));
// expected output: "Fire-Air-Water"

```

### splice - array method

The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

Example from Mozilla:

```
const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// inserts at index 1
console.log(months);
// expected output: Array ["Jan", "Feb", "March", "April", "June"]

months.splice(4, 1, 'May');
// replaces 1 element at index 4
console.log(months);
// expected output: Array ["Jan", "Feb", "March", "April", "May"]
```

### slice - array method

returns a shallow copy of a portion of a new array object where begin and end represent index of items in the array. origninal array will not be modified. if you delete it returns array with items deleted

start index, how many things you want to delete, whatever you want to insert

Example from Mozilla:

```
const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));
// expected output: Array ["camel", "duck", "elephant"]

console.log(animals.slice(2, 4));
// expected output: Array ["camel", "duck"]

console.log(animals.slice(1, 5));
// expected output: Array ["bison", "camel", "duck", "elephant"]

```

### sort - array method

sorts IN PLACE and returns the sorted array. Converts every value to string and uses utf-16 codes. mostly used with a compare function that is passed in.

```
const months = ['March', 'Jan', 'Feb', 'Dec'];
months.sort();
console.log(months);
// expected output: Array ["Dec", "Feb", "Jan", "March"]

const array1 = [1, 30, 4, 21, 100000];
array1.sort();
console.log(array1);
// expected output: Array [1, 100000, 21, 30, 4]

array1.sort(comparNumbers)  // [1,4,21,30,100000]
function compareNumbers(firstNumber, secondNumber) {
  return firstNumber - second number
}

```

### forEach

calls the function on each element. The function paramaters have access to value, index, and array.

### map

creates a new array with the results of calling a callback on every element in the array

### find

returns the value of the first element in the array that satisfies the provided testing function.

### filter

creates a new array with all elements that pass the test implemented by the provided funtion.

```
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

### every

tests whether ALL elements in the array pass the provided function. It returns a Boolean value.

### some

similar to every, but returns true if ANY of the array elements pass the test function.

### reduce

executes a reducer function on each element of the array, resulting in a single value

```
const array1 = [1, 2, 3, 4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

// 5 + 1 + 2 + 3 + 4
console.log(array1.reduce(reducer, 5));
// expected output: 15
```

### reduceRight

like reduce but starts from the end of the array

### how to check the type of array

typeof array returns 'object' so that is not really helpful

```
const arr = [1,2,]
typeof arr // object
```

Instead use Array.isArray() and pass in the array

```
Array.isArray(arr) // tre
```
