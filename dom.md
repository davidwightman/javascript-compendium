## DOM

the DOM is a JavaScript representation of a webpage

It's your JS "window" into the contents of a webpage

It's just a bunch of objects that you can interact with via JS

a programming api for documents

the bridge between html and javascript

each html tag is turned into a javascript object by the browser and stored within the DOM

document is at the top of tree

"dom is a glorified javascript object made from html on the page" - C. Williams

### Document Methods

all of the below should be done on document

```
// example: 
document.getElementById('header')
```

getElementById()

getElementsByClassName()
- this method returns an array

getElementsByTagName()
- also returns array

querySelector() + querySelectorAll()
- enter css tags

```
// example: 
document.querySelector('#header')
// if multiple instances, will only return the first

document.querySelectorAll('.li')
//would return all in an array

```

createElement()

createAttribute()

#### Other useful related methods

.document.body.appendChild(p)

.setAttributeNode()

.innerHTML
- manipulates the text in selected tag

.innerText