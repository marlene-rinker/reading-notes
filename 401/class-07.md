## Code 401 Reading Assignment Notes - Class 7

_June 16, 2020_

[Express](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-07/DISCUSSION)

### Express Routing

**Event driven system:**
- `app.get('/thing', (req,res) => {})`

- When a get event happens in our server, on "/thing", run this function. (Same pattern as in vanilla js, jquery)

**The Request Object:**
- `(req,..)`
- /:parameters
  - `app.get('/api/:thing',...)` = `req.params.thing`

- Query Strings
  - `http://server/route?ball=round` = `req.query.ball`

**The Response Object:**
- `(..., res)`

- Responsible for sending data back to the browser
- Has methods like `send()` and `status()` that Express uses to format the output to the browser properly

  - Sends Headers
    - Cookies
    - Status Codes

### Express Middleware

**What it does:**

- A series of functions that the request “goes through”

- Each function receives `request`, `response` and `next` as parameters

**Types of middleware: Application and Route**


Application Middleware:

- Error Handling
- Bringing in other routes
- Applies Defaults
- JSON, Body and Form Parsing
- Runs on every request

Route Middleware:

- Dealing with specific things for a route
- Generally, things many routes would participate in
  - Are you logged in?
  - What is your IP?
  - Have we seen you here before?

**Take advantage of Express middleware**

- Logging
- Dynamic Model Loading
- Browser, Location, User specific content
- Consistent Data Transition/Modeling/Preparation (pre-render)

**Modularization & Separation of Concerns**

- Modularizing your code into logical chunks
- Each thing should do the thing its best at
- Move files around until it feels right

**CRUD Operations with REST and Express**

CREATE
- `app.post('/resource')`

READ
- `app.get('/resource')`

UPDATE
- `app.put('/resource/:id')`

DELETE
- `app.delete('/resource/:id')`

(reading said "DESTROY" instead of "DELETE" and had the request for getting the resource by id. didn't make sense so I noted what it seems like it should be instead)

**Server Testing**
- Generally avoid starting the actual server for testing
- Instead export your sever as a module in a library
- Then use `superagent` to run your tests

[Today's main article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-07/DISCUSSION) has more details about server testing using `supertest` and `superagent`.

**Test Pyramid**
Server testing crosses boundaries:
- Units: Server Internal Functions
  - Mock any integrations (like data fetching)
- Integration: How it connects to other services
  - Really connect to other services (hard dependencies)
- Acceptance
  - The server might be a dependency of some other test

**Other Middleware Notes**

**Middleware:** Any number of functions that are invoked by the Express.js routing layer before your final request handler is made.

Middleware chain - put (req, res, next) as function parameters - next is used to pass the result of the function to the next function in the chain; optional, if used then put 'next()` in the function to go to the next function. In the above code, you run log, then hello when you go to '/'.

`app.get('/', log, hello)`

`app.use(log)` - runs every time you run the server




### Additional Resources

[Video explaining Middleware](https://www.youtube.com/watch?v=9HOem0amlyg)

[Using middleware](https://expressjs.com/en/guide/using-middleware.html)

[ExpressJS - Middleware Tutorial](https://www.tutorialspoint.com/expressjs/expressjs_middleware.htm)

[Routing](https://expressjs.com/en/guide/routing.html)

[supertest](https://github.com/visionmedia/supertest)

[Express middleware list](https://expressjs.com/en/resources/middleware.html)

[HTTP Status Codes](https://www.restapitutorial.com/httpstatuscodes.html)


---
[Home page](https://marlene-rinker.github.io/reading-notes/)