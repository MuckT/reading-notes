# Node Ecosystem, TDD, CI/CD

## Questions

### Describe (in plain English) what Array.map() does
Array.map() iterates through the array and performs the actions in map on each element. It does not mutate the array.

```JavaScript
let arr = [1,2,3,4,5]

let results = arr.map(num => console.log(num + 1))

console.log(arr) // [1,2,3,4,5]
console.log(results) // [2,3,4,5,6]
```

### Describe (in plain English) what Array.reduce() does

Array.reduce() calls a reducer on each element of the array passing the return value from the previous element. It returns the result of running the reducer on all elements of the array in a single value. It does not mutate the original array.

```JavaScript
let nestedArray = [[1,2,3],[4,5,6],[7,8,9]]

let results = nestedArray.reduce((prev, current) => [...prev, ...current])

console.log(nestedArray) // [[1,2,3],[4,5,6],[7,8,9]]
console.log(results) // [1,2,3,4,5,6,7,8,9]
```

### Provide code snippets showing how to use superagent()

```JavaScript
const superagent = require('superagent')

// With Promise .then() syntax
superagent.get('https://www.google.com/').then(console.log).catch(console.error)

// With async / await syntax
try {
  let result = await superagent.get('https://www.google.com/')
  console.log(result)
} catch(err) {
  console.error(err)
}
```

### Explain promises as though you were mentoring a Code 301 level student

Since JavaScript is single threaded and synchronous in order to prevent the blocking the execution for IO promises were created. Code that takes awhile to resolve for example a network request are call and execution continues until we have received a response for our request and the promise resolves. 

If we didn't have promises or ajax a website would require that all the images to load and external requests resolve before it would be able to be interacted with by the user.


### Are all callback functions considered to be Asynchronous? Why or Why Not?

Callbacks are not asynchronous by nature, but can be used for asynchronous purposes

#### Sources

[Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

[3 Ways to Merge Arrays in JavaScript](https://dmitripavlutin.com/javascript-merge-arrays/)

[superagent npm](https://www.npmjs.com/package/superagent)

[Understanding the Event Loop, Callbacks, Promises, and Async/Await in JavaScript](https://www.digitalocean.com/community/tutorials/understanding-the-event-loop-callbacks-promises-and-async-await-in-javascript)
