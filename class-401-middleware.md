# 401 Express REST API

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| Middleware | Functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. |
| Request Object | An object represents the HTTP request sent to an Express app. |
| Response Object | An object representing the HTTP response which is sent by an Express app when it gets an HTTP request. |
| Application Middleware | A function that is executed every time the app receives a request. |
| Routing Middleware | A function is executed every time a specific route receives a request. | 
| Test Driven Development (TDD) | A software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases. |
| Behavior Driven Development (BDD) | A software development process that encourages collaboration among developers, quality assurance testers, and customer representatives in a software project. It encourages teams to use conversation and concrete examples to formalize a shared understanding of how the application should behave. |

## Questions

### Name 3 real world use cases where you’d want to change the request with custom middleware

1. Add a timestamp to the request.
2. Add an api from the server to the request being passed through to an external API.
3. Add check the cookies are still valid.

### True or false: The route handler is middleware?

Route handlers are not middleware as they do not contain the next function as required to be middleware.

### In what ways can a middleware function end the process and send data to the browser?

Middleware can throw errors to be picked up the the error handler which will send an error response back to the browser.

### At what point in the request lifecycle can you “inject” middleware?

One can inject middleware after receiving the request and before the server sends a response, hence it can sit in the middle of a request to a server.

### What can cause express to error with “Request headers sent twice, cannot start a second response”

A great explanation can be seen on [StackOverflow](https://stackoverflow.com/a/7789131). In sum if you set the headers or response then pass to next you will likely see this error. Instead if the headers are response have been modified it's better to call `response.end()`.

## Sources

[Middleware Express](https://expressjs.com/en/guide/using-middleware.html)

[Express Request](https://www.javatpoint.com/expressjs-request)

[Express Response](https://www.javatpoint.com/expressjs-response)

[Test Driven Development](https://www.guru99.com/test-driven-development.html)

[Test Driven Development (TDD) WIKI](https://en.wikipedia.org/wiki/Test-driven_development)

[Behavior Driven Development (BDD)](https://www.guru99.com/bdd-testing-rest-api-behave.html)

[Behavior Driven Development (BDD) WIKI](https://en.wikipedia.org/wiki/Behavior-driven_development)
