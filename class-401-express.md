
# 401 [Express](https://expressjs.com/)

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| Web Server | A web server is computer software and underlying hardware that accepts requests via HTTP. |
| Express | A fast minimalist web framework for Node.js applications. |
| Routing | Routing refers to determining how an application responds to a client request to a particular endpoint and a specific HTTP request method. |
| Web Request Response Cycle (WRRC) | The web is a cycle of requests and responses that flow between clients and servers. |
 

## Questions

### What’s the difference between PUT and PATCH?

- PUT is used to entirely update an resource whereas PATCH sends data to partially replace the resource it does not modifying the entire resource.

### Provide links to 3 services or tools that allow you to “mock” an API for development like json-server?
1. [Jest Mocking](https://www.valentinog.com/blog/fake/#mocking-fetch-with-jest)
2. [Cypress Mocking](https://docs.cypress.io/guides/guides/network-requests#Stub-Responses)
3. [Nock](https://www.npmjs.com/package/nock)
 

### Compare and contrast Swagger and APIDoc.js

| Swagger (UI Dist) | APIDocs.js | 
| ---- | ---- |
| 792k weekly downloads | 75k weekly downloads |

### Which HTTP status codes should be sent with each type of (un)successful API call?

3xx is a redirection error
4xx is a client error
5xx is a server error


### Compare and contrast SOAP and ReST
| SOAP | REST |
| ---- | ---- |
| Multiple Protocols| HTTP & HTTPS |
| Protocol | Architecture |
| XML Only | HTML, JSON & XML |

## Sources

[Web Server](https://en.wikipedia.org/wiki/Web_server)

[Express Glossary](https://expressjs.com/en/resources/glossary.html)

[Routing](https://expressjs.com/en/starter/basic-routing.html)

[Web Request Response Cycle (WRRC)](https://medium.com/@jen_strong/the-request-response-cycle-of-the-web-1b7e206e9047)

[PUT & PATCH](https://rapidapi.com/blog/put-vs-patch/)

[SOAP VS REST](https://raygun.com/blog/soap-vs-rest-vs-json/)
