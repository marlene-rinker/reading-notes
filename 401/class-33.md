## Code 401 Reading Assignment Notes - Class 33

_July 22, 2020_

### Context API

[Context API](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-33/DISCUSSION)


Context provides a means of passing state down the component tree through a Provider/Consumer relationship.

At as high a level as makes sense, a “provider” can make it’s state available, along with means of altering it (methods).

At the lower levels any component can “opt-in” and become a “consumer” and receive `this.state` from context.

In a **class style component**, you can attach to context in 2 ways:

- Wrap your component with, and use a function to “get” the context object itself, which is `this.state` from the provider component.

- Statically declare a connection to the context provider and then use `this.context` to connect to state from the context provider.

In a **functional component**, you can use the `useContext()` hook to tap right in.

It returns and provides access to whatever your context provider exports.


_Note_ – the context API is still critically important even with this hook available. Not every React shop is using hooks, so know both ways.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-33/DISCUSSION) shows code examples.

Context provides a way to pass data through the component tree without having to pass props down manually at every level.

Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

#### Additional Resources

[Context - React guide](https://reactjs.org/docs/context.html)

[Hooks and Context Example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)

[Awesome React Context - Resource Links](https://github.com/diegohaz/awesome-react-context)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)