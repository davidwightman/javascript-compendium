## DOM

the DOM is a JavaScript representation of a webpage

It's your JS "window" into the contents of a webpage

It's just a bunch of objects that you can interact with via JS

a programming api for documents

the bridge between html and javascript

each html tag is turned into a javascript object by the browser and stored within the DOM

document object is at the top of tree

"dom is a glorified javascript object made from html on the page" - C. Williams

### Document Methods

all of the below should be done on document

getElementById()

```
// example: 
document.getElementById('header')
```

getElementsByClassName()
- this method returns an array-like collection. HTMLCollection

getElementsByTagName()
- also returns array-like object that is not array. it is an HTMLCollection. you can use array indexes (brackets). however array methods DO NOT work. just .length works. you can iterat over it with a for of loop. you can however spread into an array 
```
const inputs = document.getElementsByTagName('input')
const arr = [...inputs]
```

querySelector() + querySelectorAll()
- enter css selector
- element or...
- id or...
- class

```
// example: 
document.querySelector('#header')
// if multiple instances, will only return the first

document.querySelectorAll('.li')
//would return all in an array
// returns a NodeList, an array-like object
```

createElement()

createAttribute()

#### Other useful related properties and methods

.document.body.appendChild(p)

.setAttributeNode()

.innerHTML
- returns text AND all other tags
- manipulates the text in selected tag
- if you are adding tags you need to set it all as one string.

.innerText
- get all of the text inside of it, no matter how many elements. you cannot create new elements. use innerHTML to create new elements

.textContent
- like innerText but preserves spacing, and script text if included. would also show text with style display: none. So, basically just cuts out the tags.
