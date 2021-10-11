# 401 Data Modeling

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| Functional Programming (FP) | The programming paradigm achieved by composing pure functions, avoiding shared state, mutable data, and side-effects. |
| Pure Function | Given the same input it always returns the same output. Produces no side effects. |
| Shared State | A variable that can be accessed from more than one function. |
| Object-oriented Programming | a programming paradigm which tries to emulate real world problems using the abstract concept of ‘objects’ as a data structure which can be mutated and referenced.|
| Class | A template for creating objects. They encapsulate data with code to work on that data.|
| `super` | A keyword used to access and call functions on an object's parent. |
| `this` | References the object of which the function is a property; this references the object that is currently calling the function. |
| Test Driven Development | A software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases. |
| Jest | JavaScript testing framework designed to ensure correctness of any JavaScript codebase. |
| Continuos Integration (CI) | The practice of automating the integration of code changes from multiple contributors into a single software project.| 
| Representational State Transfer (REST) | A software architectural style is designed for network-based applications, specifically client-server applications. |
| Data Model | An abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.|

## Questions

### Name 3 advantages to Test Driven Development.

1.  The software design becomes more modular.
2.  The Code is documented better.
3.  Reduction in total hours spent on testing and maintenance activities.

### In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?

One might use `beforeEach()` to set up the test state prior to running the tests such as seeding the database. `afterEach()` is commonly used to clean-up state to prevent a build up of state as test suites are run.

### What is one downside of Test Driven Development?

One downside of Test Driven Development as that when it is first implemented it will significantly slow down development as developers adjust and tech debt around unit tests is paid off.

### What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

ES6 classes are primarily syntactical sugar over JavaScript’s existing prototype-based inheritance.

### Why REST?

 - REST is much easier to implement than approaches such as SOAP & GraphQL.
 - REST is based on standard HTTP operations.
 - REST APIs provide a great deal of flexibility.
 - REST APIs are Stateless on the server-side.


## Sources

[Master the JavaScript Interview: What is Functional Programming?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)

[What is Functional Programming? Tutorial with Example](https://www.guru99.com/functional-programming-tutorial.html)

[Master the JavaScript Interview: What is a Pure Function?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976)

[What Is Object Oriented Programming?](https://medium.com/swlh/what-is-object-oriented-programming-f5b42f3ac826)

[Class MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

[`super` MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)

[`this`](https://www.javascripttutorial.net/javascript-this/)

[Test Driven Development (TDD)](https://www.guru99.com/test-driven-development.html)

[Jest](https://jestjs.io/)

[Continuous Integration (CI)](https://www.atlassian.com/continuous-delivery/continuous-integration)

[Representational State Transfer (REST) Wiki](https://en.wikipedia.org/wiki/Representational_state_transfer)

[Data Model Wiki](https://en.wikipedia.org/wiki/Data_model)

[What are the advantages of test-driven development?](https://fortegrp.com/test-driven-development-benefits/)

[Javascript : Prototype vs Class](https://medium.com/@parsyval/javascript-prototype-vs-class-a7015d5473b)

[The Benefits of Going RESTful – What is REST and Why You Should Learn About It](https://www.freecodecamp.org/news/benefits-of-rest/)
