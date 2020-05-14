## Code 301 Reading Assignment Notes - Class 9

_May 14, 2020_

### Functional Programming

[Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

Functional programming is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects.

#### Pure Functions

A pure function returns the same result if given the same arguments (also referred as deterministic). It does not cause any observable side effects.

Functions that read external files or relies on random numbers are not pure.

Pure functions are easier to test.

#### Immutability

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

#### Referential Transparency

If a function consistently yields the same result for the same input, it is referentially transparent.

pure functions + immutable data = referential transparency

#### Functions as First-class Entities

The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.

#### Higher-order Functions

When we talk about higher-order functions, we mean a function that either takes one or more functions as arguments, or
returns a function as its result.

`filter`, `map`, and `reduce` can be higher-order functions.

#### Other Resources

[Functional Programming Repository](https://github.com/leandrotk/functional-programming-learning-path)

[Code from this article](https://github.com/tk-notes/fp-in-javascript-article-source-code)

### Refactoring

[Refactoring JavaScript for Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

#### Strategies for creating clean code

- Return early from functions

- Cache variables so functions can be read like sentences

- Check for Web APIs before implementing your own functionality











---
[Home page](https://marlene-rinker.github.io/reading-notes/)