## Async

### Promises

A promise is an object representing the eventual completion or failure of an asynchronous operation.

```
const newPromise = new Promise((res, rej) => {
    if (){
        res()
    } else {
        rej()
    }
})
// you can put this in a function and return it

newPromise.then(() => { 
    console.log('hi')
}).catch(() => {
    console.log('reject was called')
})
```

A promise is a returned object to which you attach callbacks, instead of passing callbacks into a function.

promise status
pending
fufilled
rejected - failed

### AJAX

XML - like html. broad way of grouping content and adding meaning to data (needs more detail)

JSON