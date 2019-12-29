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

#### Fetch

promise-based
catch does not work on 404 or 500 - must check response.status
If working with JSON you must add .json() to response to parse the stream

#### Axios

uses fetch behind the scenes
promise-based
parses json data for you
catch works for 404

### Async Await

- async functions always return a promise
- if the function returns a value, the promise will be resolved to that value
- if the function throws an exception, the promise will be rejected



