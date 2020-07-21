## Code 401 Reading Assignment Notes - Class 32

_July 21, 2020_

### Custom Hooks

[Custom Hooks](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-32/DISCUSSION)


Custom Hooks:

- extract duplicated logic from components
- share common functionality, but not state
- take advantage of useEffect lifecycle

Common use cases - make things DRY

- handle forms easily
- pre-fetch API data
- connect to services (like socket.io, Q, etc.)

Unlike a React component, a custom Hook doesn’t need to have a specific signature. We can decide what it takes as arguments, and what, if anything, it should return. In other words, it’s just like a normal function. Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-32/DISCUSSION) has a simple example of coding and using a custom hook.

#### Additional Resources

[Custom Hooks - all you need to know](https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)

[Async Hooks](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)

[useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)

[React Custom Hooks](https://reactjs.org/docs/hooks-custom.html)

[useHooks - React Hook Recipes](https://usehooks.com/)

[Hooks List - awesome react hooks resources](https://github.com/rehooks/awesome-react-hooks)

[10 Essential React Hooks](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)