## Code 401 Reading Assignment Notes - Class 12

_June 23, 2020_

[OAuth](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-12/DISCUSSION)

### OAUTH2.0

Officially, OAuth is “an open standard for access delegation” … In other words, OAuth serves as a way to give users the ability to grant application access to services, without giving the application their password.

Example: Login with Google

#### How does OAuth work?

Through a series of “handshakes”, an application such as an Express Web Server asks the user if it’s ok to login as them at some remote service, and then begins the process of authentication and access.

1. Application spawns the “Login Using xxx” window, asking for specific permissions

2. User Agrees to allow this to happen

3. Remote service (i.e. Google) contacts the application with a one-time-use `Code`

4. The application calls back to a special address on the remote service to exchange that `Code` for a `Token`

5. Once the token has been granted, the application will then be able to contact the remote service, using that `Token` to access information on behalf of the user

The `token` is the user.

#### Access Code
First the client needs to grant the application permission. To do this you need to provide an `<a>` tag that will take them to the service’s authorization page. This `<a>` tag should pass the following information through a query string to the authorization server. Every service is slightly different in their specific requirements, but in some form or another, variables like these are part of this initial request

- `response_type=code` indicates that your server wants to receive an authorization code

- `client_id=<your client id>` tells the authorization server which app the user is granting access to

- `redirect_uri=<your redirect uri>` tells the auth server which server endpoint to redirect to

- `scope=<list of scopes>` tells the auth server what you want the user to give access to

- `state=<anything you want>` a place where you can store info to pass to your server if you want

#### Access Token

If the user grants access to the application, the authorization server will redirect to a provided redirect URI callback with a “code”. Once you have this code, you can exchange it for an access token by making a `POST` request to the authorization server and providing the following information:

- `grant_type=authorization_code`

- `code=<the code your received`

- `redirect_uri=REDIRECT_URI` must be same as the redirect URI your client provided

- `client_id=<your client id>` tells the authorization server which application is making the request

- `client_secret=<your client secret>` authenticates that the application making the request is the application registered with the `client_id`

- Once you get an access token, you can use it to make API calls to the service on behalf of that user

#### Other Notes

OAuth is used for authorization not authentication. It was created for a service to authorize another service.

OAuth2.0 is the most widely used version today.

OAuth authorizes on your behalf with your permission.

OAuth access token - contains user-allowed permissions; secure and can be verified; JWT is the format for the access token



### Additional Resources

[OAuth 2 Simplified](https://aaronparecki.com/oauth-2-simplified/)

[OAuth Video](https://www.youtube.com/watch?v=t4-416mg6iU)

[OAuth wiki](https://en.wikipedia.org/wiki/OAuth)

[Build a Node API with OAuth 2](https://developer.okta.com/blog/2018/08/21/build-secure-rest-api-with-node)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)