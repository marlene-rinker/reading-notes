## Code 301 Reading Assignment Notes - Class 6

_May 11, 2020_

### Node.js

[An Introduction to Node.js](https://www.sitepoint.com/an-introduction-to-node-js/)

Node.js is built on Google Chrome's V8 JavaScript engine. It's a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

The article has instructions for installing Node.js.

Node is bundled with a JavaScript package manager called npm.

In addition to being the package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week.

The article has instructions for installing packages using npm.

`node_modules` is one of the folders you get when you install a package. This is where the package and any libraries that it depends on live. This folder shouldn't be checked in to version control.

Node and npm are important for installing (npm) and running (via Node) various build tools. 

The article contains links to articles covering build tooling.

Node.js, however, is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event.

Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. Node.js even has a built-in module to help you implement a cloning strategy on a single server.

Node is particularly suited to building applications that require some form of real-time interaction or collaboration

It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven (such as those needing to perform operations on a database), or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded. 

Advantages of Node.js are:

- you do everything in the same language

- it speaks JSON which is probably the most important data exchange format on the Web

- most developers are familiar with JavaScript

In conclusion, Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

---
[Home page](https://marlene-rinker.github.io/reading-notes/)
