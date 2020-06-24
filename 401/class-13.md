## Code 401 Reading Assignment Notes - Class 13

_June 24, 2020_

[Bearer Authorization](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-13/DISCUSSION)

### Bearer Authentication

Rather than continually sending username+password over the internet, or undergoing the long OAuth process, we are able to use a secondary authentication method called “Bearer Token”

Bearer Tokens are encoded JSON objects that “bear” or “contain” enough information for the server to assert that any client request that presents a valid token must have originated from a client that has previously authenticated themselves using either Basic or OAuth. Upon receiving a Bearer Token from a client, the server can decode it, inspect the JSON object inside, look up the appropriate account, and re-authenticate the user in a single lookup.

- Bearer Tokens are sent to the user/client after the initial signin process has completed.

- Clients must make every subsequent request to the server with that token, in the header

  - `Authorization: Bearer encoded.jsonwebtoken.here`

- The server opens the token, does the re-authentication, and then grants or denies access

- In express servers, this can be done in middleware, in conjunction with a user model

### JSON Web Tokens

JSON Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transmitting information between parties (servers, clients, etc) as a JSON object.

Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

Signing a token does not secure it’s contents. They are viewable, so be careful of the information that you include in the JSON data. A properly signed token is verified.

The most common scenario for using JWT is for authorization. Single Sign On widely uses JWT because of its small overhead and its ability to be easily accessed across different domains.

JWT is also used for information exchange. It's a good way of securely transmitting information between parties.

### Additional Resources

[JWT Explained Video](https://www.youtube.com/watch?v=926mknSW9Lo)

[Intro to JWT](https://jwt.io/introduction/)

[Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

[npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)