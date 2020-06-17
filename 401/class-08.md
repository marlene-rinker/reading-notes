## Code 401 Reading Assignment Notes - Class 8

_June 17, 2020_

### Express Routing & Connected API

Routes can be managed in separate modules from the main server. This allows us to extract that logic and wiring to be more topical.

- index.js - Entry point

- server.js - Hub, Exported server

- models/categories.js, etc. - Data models

- routes/categories.js, etc. - Routers and Handlers

Routing refers to how an application’s endpoints (URIs) respond to client requests.

[The Express guide](https://expressjs.com/en/guide/routing.html) has some good routing information.

The order you place your middleware and routes is very important. Everything will happen in the order that they appear. This means that if you place your middleware after a route, then the route will happen before the middleware and the request will end there. Your middleware will not run at that point.



### Additional Resources

[Using Express Routing Guide](https://expressjs.com/en/guide/routing.html)

[Express Router Tutorial](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)


---
[Home page](https://marlene-rinker.github.io/reading-notes/)