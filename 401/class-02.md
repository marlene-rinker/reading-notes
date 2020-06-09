## Code 401 Reading Assignment Notes - Class 2

_June 9, 2020_

### Node Ecosystem, TDD, CI/CD

_Sources_

[codica TDD article](https://www.codica.com/blog/test-driven-development-benefits/)

[Jest documentation](https://jestjs.io/docs/en/setup-teardown)

[Lean Testing - pros and cons](https://leantesting.com/test-driven-development/)

[JS Developer article](https://www.toptal.com/javascript/es6-class-chaos-keeps-js-developer-up#:~:text=Prototypes%20vs.,is%20itself%20an%20object%20instance.&text=A%20constructor%20in%20JavaScript%20is,function%20that%20returns%20an%20object.)

[JavaScript Info - static methods](https://javascript.info/static-properties-methods)

[Bits and Pieces Blog](https://blog.bitsrc.io/understanding-higher-order-functions-in-javascript-75461803bad)

[Functional Programming](https://www.sitepoint.com/what-is-functional-programming/)
 
[Medium -higher order functions](https://medium.com/javascript-scene/higher-order-functions-composing-software-5365cf2cbe99#:~:text=A%20higher%20order%20function%20is,map()%20and%20.)

[Toward data science article](https://towardsdatascience.com/javascript-context-this-keyword-9a78a19d5786)

[Wikipedia](https://en.wikipedia.org/wiki/Continuous_integration)


_**Name 3 advantages to Test Driven Development.**_ 

1. Better program design and higher code quality
2. Detailed project documentation
3. TDD reduces the time required for project development


_**In what case would you need to use `beforeEach()` or `afterEach()` in a test suite?**_
When you have work to do repeatedly for many tests.

_**What is one downside of Test Driven Development?**_ It necessitates a lot of time and effort up front, which can make development feel slow to begin with.

_**What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?**_
A class defines a type which can be instantiated at runtime, whereas a prototype is itself an object instance.

_**Name a use case for a static method.**_ Usually, static methods are used to implement functions that belong to the class, but not to any particular object of it.

_**Write an example of a Higher Order function and describe the use case it solves**_

This .map function calculates ages based on a birth year. It's a function that takes in another function, such as a callback function.

```
const birthYear = [1975, 1997, 2002, 1995, 1985];

const ages = birthYear.map(year => 2020 - year);

// prints [ 45, 31, 18, 25, 35 ]
console.log(ages);
```



#### Vocabulary Terms

**functional programming** - Functional programming is a paradigm, or style, that values immutability, first-class functions, referential transparency, and pure functions.

**higher-order function** - A higher order function is a function that takes a function as an argument, or returns a function.

**immutable state** - An immutable object is an object that can’t be modified after it’s created.

**object** - a self-contained entity that consists of both data and procedures to manipulate the data.

**object-oriented programming (OOP)** - Object-oriented programming (OOP) refers to a type of computer programming (software design) in which programmers define the data type of a data structure, and also the types of operations (functions) that can be applied to the data structure.

**class** - In JavaScript, classes are in fact "special functions".

**prototype** - Prototypes are the mechanism by which JavaScript objects inherit features from one another. 

**`super`** - The super keyword is used to access and call functions on an object's parent.

**inheritance** - "child" object classes (constructors) inherit features from their "parent" classes

**instance** - An object created by a constructor is an instance of that constructor.

**context** - Context is always the value of the this keyword 

**`this`** - a reference to the object that “owns” the currently executing code or the function where it’s looked at

**Test Driven Development (TDD)** - Test Driven Development is a software development practice enabling developers to create proper specifications about how their code should be written and implemented. 

**Jest** - Jest is a delightful JavaScript Testing Framework with a focus on simplicity.

**Continuous Integration (CI)** - In software engineering, continuous integration (CI) is the practice of merging all developers' working copies to a shared mainline several times a day.

**unit test** - testing a certain behavior


### Additional Resources

[MDN-Inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain) 

[MDN-this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

[MDN-classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

[Node.js errors](https://nodejs.org/dist/latest-v6.x/docs/api/errors.html)

[Jest docs](https://jestjs.io/docs/en/getting-started)



---
[Home page](https://marlene-rinker.github.io/reading-notes/)