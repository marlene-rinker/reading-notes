## Code 401 Reading Assignment Notes - Class 36

_July 27, 2020_

### Application State with Redux

[Application State with Redux](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-36/DISCUSSION)

Managing state with Redux requires the combination of 3 distinct aspects into a “Store” which all components can access as they please.

- State

- Reducers (strategies to alter state)

- Actions (methods that get “dispatched” or “run”, which trigger associated reducers)

#### Redux Store

The **store** is where your application state is stored. The store's job is to identify the various reducers and middleware that need to be made available and used globally.

React uses **reducers** to hold and manage state. Reducers typically manage just one part of the larger application state. For example, in a storefront application, you'd probably have a separate reducer for Products, Categories, and Carts. 

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-36/DISCUSSION) has sample code and an explanation of a reducer for a shopping cart.

React applications with Redux dispatch **actions** (like an event) with _payload_ (data). An action creator function always returns an action object with the action type to perform and the data to perform it with. When your component wants to modify state, it _Dispatches_ (calls) an action and sends whatever _payload_ (data) it needs to, to the reducer.

When an action is dispatched, a reducer responds to it, and receives that payload, where it then operates on state using it.

We use a store to bring it all together. In the store, you declare what middleware you may need and the reducers that you’ll use to manage your state data.

Components subscribe to the store and get to use actions with a bit of boilerplate code.

Before any of this can work, your entire application needs to be given access to the store.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-36/DISCUSSION) has a good explanation and sample code for how this works.

#### More Notes
Everything that changes in your application including the data and UI state is contained in a single object called the state or the state tree.

The state tree is redundant - you can't modify or write to it. Anytime you want to change the state you need to dispatch an action. An action is a plain javascript object describing the change. It must have a **type** property which is not undefined. It's recommended that this is a string.


#### Additional Resources

[Dan Abramov Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)

[World's easiest guide to Redux](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6/)

[Testing with Redux and Enzyme](https://medium.com/netscape/testing-a-react-redux-app-using-jest-and-enzyme-b349324803a9)

[Testing Reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)

[Redux docs](https://redux.js.org/)

[Enzyme-redux npm module](https://www.npmjs.com/package/enzyme-redux)

[Middleware tests with a mock store](https://gist.github.com/johncokos/4902683c8e33ed38fb2ba066b8764831)










---
[Home page](https://marlene-rinker.github.io/reading-notes/)