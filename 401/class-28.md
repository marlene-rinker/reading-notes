## Code 401 Reading Assignment Notes - Class 28

_July 15, 2020_

[Props and State](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-28/DISCUSSION)

#### Forms and Inputs

React form elements maintain internal state. Think of React inputs as stateful child components.

The creation of a parent component (which we’ll refer to as form-container), manages the state for all child components of the form and passes any necessary state down into its inputs through the use of `props`. Each input has an `onChange` event that we can handle and use to update our form-container’s state each time the user interacts with an input.

**Props**

Components accept arbitrary inputs called `props`. In JSX, `props` are passed into a component with a syntax that looks like HTML attributes. These are the equivalent of function params.

In actuality, `props` is the name of the object passed into a component constructor and any prop added to a component in the JSX will be accessible as a property on `props`.

After `props` is passed into the constructor's `super` function, they are available on the context by using `this.props`.

Props can be data or functions.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-28/DISCUSSION) has a code example and explanation.

**One Way Data Flow**

State can only be passed from parent component to a child component through the use of `props`. This enforces the idea of one way data flow. One way data flow is a way of describing that state can only be passed down the component tree (not up). If a child wants to pass some data to a parent, the parent can pass a function to the child through `props` and the child may invoke that function and pass it data for the parent to manage.

#### Additional Resources

[setState - React](https://css-tricks.com/understanding-react-setstate/)

[Handling Events - React](https://reactjs.org/docs/handling-events.html)

[Forms - React](https://reactjs.org/docs/forms.html)

[State and Lifecycle - React](https://reactjs.org/docs/state-and-lifecycle.html)

[Components and Props - React](https://reactjs.org/docs/components-and-props.html)




---
[Home page](https://marlene-rinker.github.io/reading-notes/)