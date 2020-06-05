## Code 401 Reading Assignment Notes - Class 1

_June 8, 2020_

### Node Ecosystem, TDD, CI/CD

_Sources_

[npm documentation](https://docs.npmjs.com/)

[Introduction to Node.js](https://www.sitepoint.com/an-introduction-to-node-js/)

[Beginners Guide to npm](https://www.sitepoint.com/beginners-guide-node-package-manager/)

[WhatIs.com](https://whatis.techtarget.com/)

[Dictionary.com](https://www.dictionary.com/)

[TechTerms](https://techterms.com/)

[Use Module.exports to keep Node.js Code Organized](https://medium.com/@osiolabs/use-module-exports-to-keep-node-js-code-organized-9379526ebac8)


_**Why would you want to run JavaScript code outside of a browser?**_ You want to perform tasks on the webserver. You don't want the source code to be visible to the user. You want to create web pages dynamically. You want to access data from a database or API.


_**What is the difference between a module and a package?**_
A package is a file or directory that is described by a package.json file.
A module is any file or directory in the node_modules directory that can be loaded by the Node.js require() function.
Note: Since modules are not required to have a package.json file, not all modules are packages. Only modules that have a package.json file are also packages.

_**What does the node package manager do?**_ It's a software registry that allows developers to share code that solves a problem and allows other developers to use that code. This reusable code is called a package.

_**Provide code snippets showing 3 different ways to export a function from a node module.**_
For these examples, we'll export functions from helpers.js file and use them in index.js.

```
//Exporting a single function

// helpers.js
module.exports = function(x) {
  return x * 2
}

// index.js
const helpers = require('./helpers.js')
helpers(4) // => 8
```
```
//Exporting several functions at once using an object literal that holds the functions

// helpers.js
module.exports = {
  multiplyByTwo: function(x) { return x *2 },
  divideByTwo: function(x) { return x / 2}
}

// index.js
const helpers = require('./helpers.js')
helpers.multiplyByTwo(10) // => 5

// or, you can import just the named property you need
const divideByTwo = require('./helpers.js').divideByTwo
divideByTwo(18) // => 9
```

```
//A different syntax for exporting several functions at once using an object literal

// helpers.js
module.exports.multiplyByTwo = function(x) { return x * 2 }
module.exports.divideByTwo = function(x) { return x / 2 }
function nonExportedFunction(x) {
  return x * 3
}

// index.js
const helpers = require('./helpers.js/)
const divideByTwo = require('./helpers.js').divideByTwo
```




#### Vocabulary Terms

**ecosystem** - a system or network of interconnecting and interacting parts

**Node.js** - a program used to execute JavaScript on the computer instead of in the browser

**V8 Engine** - the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.

**module** - any file or directory in the node_modules directory that can be loaded by the Node.js require() function. A module must be one of these: a folder with a package.json file containing a "main" field, a folder with an index.js file in it, or a JavaScript file.

**package** - a file or directory that is described by a package.json file. It must contain a package.json file in order to be published to the npm registry.

**node package manager (`npm`)** - package manager for JavaScript that is also the world's largest software registry; it allows developers to share and borrow packages.

**server** - a computer that provides data to other computers

**environment** - combination of hardware and software in a computer

**interpreter** - a program that reads and executes code in a single step; 

**compiler** - a program that compiles source code files into an executable program.



### Additional Resources

[What is npm](https://docs.npmjs.com/about-npm/index.html) 

[npm documentation](https://docs.npmjs.com/)



---
[Home page](https://marlene-rinker.github.io/reading-notes/)