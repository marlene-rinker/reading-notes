## Code 401 Reading Assignment Notes - Class 11

_June 22, 2020_

[Authentication](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-11/DISCUSSION)



### User Modeling

It's a developer's responsibility to store sensitive information responsibly.

Some information, like emails, user names, and addresses can be stored in plain text, as long as the database is password protected and/or behind a firewall. 

Other information, like a user's password, should be encrypted using a hashing algorithm before it is ever stored. This prevents anyone (including developers with database permissions) from ever getting access to their password.

User models that have sensitive data that should NEVER be sent to client applications.

### Cryptography

Cryptography is the science which studies methods for encoding messages so that they can be read only by a person who knows the secret information required for decoding, called the key.

### Hash Algorithms

A Cryptographic Hash Algorithm takes a piece of data and produces a hash that is deliberately difficult to reverse. If identical data is passed into the algorithm the same hash will always be produced. Hash algorithms are often used for checking the integrity of data.

### Cypher Algorithms

A Cryptographic Cypher Algorithm takes a piece of data and a key and produces encrypted data. Later the encrypted data can be reversed into the original data by decrypting it using the same key.

### Basic Authorization

Basic Authorization is a common method used to send a username and password in an HTTP request. The username and password are joined with a ‘:’ then “base64 encoded” and placed after the string ‘Basic ‘. The resulting string is set to the value of an Authorization header.

The client and server must use HTTPS to protect the username and password as it travels across the network.

In browsers, we get `atob` and `btoa` to convert to/from "Base64 Encoding."

```
let encoded = window.btoa('someusername:P@55w0rD!')
// c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==

let decoded = window.atob('c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==');
// someusername:P@55w0rD!

request({
  method: 'GET',
  url: 'https://api.example.com/login',
  headers: {
    Authorization: `Basic ${encoded}`,
  },
})
.then(handleLogin)
.catch(handleLoginError)

```

In a node application, we can use a node module to do the same work (those methods are not built-in).

```
let base64 = require('base-64');

let string = 'someusername:P@55w0rD!';
let encoded = base64.encode(string); // c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==
let decoded = base64.decode(encoded); // someusername:P@55w0rD!

```




### Additional Resources

[GNU Collaborative International Dictionary of English](https://gcide.gnu.org.ua/)

[Securing Passwords](http://cs.wellesley.edu/~cs304/lectures/bcrypt/dustwell.html)

[Basic Access Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication)

[Introduction to JSON Web Tokens](https://jwt.io/introduction/)

[Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

[bcrypt documentation](https://www.npmjs.com/package/bcrypt)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)