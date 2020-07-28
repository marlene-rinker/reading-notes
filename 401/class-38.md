## Code 401 Reading Assignment Notes - Class 38

_July 29, 2020_

### Redux - Asynchronous Actions

[Redux - Asynchronous Actions](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-38/DISCUSSION)

#### Using Redux actions to connect to remote APIs via Thunk Middleware (Thunking for Data)

Normally, action generators return a function. But often, you’ll need your actions to do some asynchronous action before you dispatch it to the reducer. For example, you may need to get something from a remote api.

In this case, we want to set it up where the action you dispatch from your React App returns a function, not an actual action object, which is what Redux expects and requires.

Special redux middleware, called “thunk”, inspects every dispatched action and then either lets it go through (in the case of a normal action that returns an object) or it processes the function and then dispatches what that function returns.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-38/DISCUSSION) has code examples.

We'll be using the `redux-thunk` npm module since it provides more stability and error checking.




#### Additional Resources

[Async Actions - Redux](https://redux.js.org/advanced/async-actions)

[Thunk Middleware](https://github.com/reduxjs/redux-thunk)

[Redux Thunk](https://www.digitalocean.com/community/tutorials/redux-redux-thunk)

[React Suspense](https://blog.logrocket.com/async-rendering-in-react-with-suspense-5d0eaac886c8/)




---
[Home page](https://marlene-rinker.github.io/reading-notes/)