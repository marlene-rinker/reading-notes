## Code 401 Reading Assignment Notes - Class 6

_June 15, 2020_

[HTTP and REST](http://codefellows.github.io/code-401-javascript-guide/curriculum/class-06/DISCUSSION.html)

### HTTP

The Hyper Text Transfer Protocol (HTTP) is the foundation for the world wide web. Applications built using HTTP subscribe to the client-server computing model. In the client-server computing model a host designed to provide a service is called a server. Clients are hosts that make requests to that service.

#### HTTP Requests

A HTTP/1.1 request is formatted in text and transferred using TCP. The first line of the request contains the `METHOD`, `URL`, and `HTTP VERSION`. The following lines are the request `HEADERS`. Each header is separated by a newline character. A header is a key value pair separated using a colon. Headers containing more than one value separate each value using a semicolon. The header section of the request is terminated with an empty line. An optional body follows the header section. 

The [HTTP and REST article](http://codefellows.github.io/code-401-javascript-guide/curriculum/class-06/DISCUSSION.html)  has a helpful table that has details about the different requests that you can make.

New terminology for HTTP Requests:

`Safe` methods should only be used for information retrieval and should not change the server state.

`Idempotent` methods means if two identical requests are made they should get an identical response. 

`Cacheable` means the client should be able to cache the response.

Example:
```
POST /api/note HTTP/1.1
Host: api.example.com
Origin: www.example.com
Authorization: Bearer bHVsIHRoaXMgaXMgYSBmYWtlIHNlY3JldCB0b2tlbg==
Accept: application/json
Content-Type: application/json; charset=UTF-8
Content-Length: 58

{"title":"kata","content":"get 100 points on hacker rank"}
```

#### HTTP Response

A HTTP/1.1 response is also formatted in text and transferred using TCP. The first line of the response contains the `HTTP VERSION`, `STATUS CODE`, and `STATUS MESSAGE`. The following lines are the request headers and are formatted exactly the same way as the request headers. The header section of the request is terminated with an empty line. An optional body follows the header section.

Example:

```
HTTP/1.1 200 OK
Date: Tue, 22 Aug 2017 06:34:16 GMT
Content-Type: application/json; charset=UTF-8
Content-Encoding: UTF-8
Content-Length: 82
Last-Modified: Mon, 21 Aug 2017 12:10:38 GMT
Server: Apache/1.3.3.7 (Unix) (Red-Hat/Linux)
ETag: "3f80f-1b6-3e1cb03b"
Connection: close

{"id":"1234123412341324","title":"kata","content":"get 100 points on hacker rank"}
```

#### REST

REST is acronym for REpresentational State Transfer. In layman’s terms, is a means by which we can reference, manipulate, and transfer state. A “RESTful Endpoint” is a URI that identifies the resource.


RESTful Endpoint: `http://api.server.com/api/v1/people`

`http://` - Protocol/Scheme

`api.server.com` - Domain or Server

`/api/v1` - API Endpoint

`/people` - The resource (This identifies a collection: all people)

`/people/12345` - A more specific resource: The person with id 12345

**REST Method - CRUD Operation - Function**

GET - READ - Retrieve 1 or More Records

POST - CREATE	- Create a new record

PUT - UPDATE - Update a record through replacement (Put it back)

PATCH - UPDATE - Update a record (just the parts that changed)

DESTROY - DELETE - Remove a record

#### REST Documentation
The standard for documenting REST APIs is with a “live” documentation system: Open API (formerly “Swagger”).

 [Open API and Swagger](https://swagger.io/docs/specification/about/)

**OpenAPI Specification**: a broadly adopted industry standard for describing modern APIs

**Swagger**: a set of open-source tools built around the OpenAPI Specification that can help you design, build, document and consume REST APIs. 

Once generated, Swagger Docs present developers a way not only see how to use an API, but to actually use it. 

[Example Docs from Swagger](https://app.swaggerhub.com/apis/ahardia/swapi/1.0.0#/)

The swagger documentation service allows you to generate the swagger documentation simply by visiting your API and analyzing the output.

[Swagger.io](https://swagger.io/)

The [HTTP and REST article](http://codefellows.github.io/code-401-javascript-guide/curriculum/class-06/DISCUSSION.html) has steps for creating documentation using Swagger.


### Additional Resources

[Video explaining HTTP and REST](https://www.youtube.com/watch?v=Q-BpqyOT3a8)

[HTTP Basics](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)

[What is REST](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)

[Swagger Documentation](https://swagger.io/docs/)

[Swagger Editor](https://editor.swagger.io/)

[HTTP reference](https://code-maze.com/the-http-reference/)

[REST reference](https://www.restapitutorial.com/lessons/httpmethods.html)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)