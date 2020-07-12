## Code 401 Reading Assignment Notes - Class 26

_July 13, 2020_

[Component Based UI](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-26/DISCUSSION)

### Component Based UI Systems

Component based UI systems like React, Angular, Vue and the like all operate on similar architectural principles.

Rather than view an application as an enormous interconnected codebase, the application is a **composition** of **components** that work together to make the application work.

The secret sauce is how they work together.

We use Classes and Functions to classify functionality.

We require what we need.

We render it where we want.

We pay attention to **state** and react as it changes.

In our class, we'll be using **React**.

### JSX

JSX is a syntax extension to JavaScript. Use it with React to describe what the UI should look like. JSX produces React “elements”. 

### Elements

Elements are the smallest building blocks of React apps.

An element describes what you want to see on the screen:

```
const element = <h1>Hello, world</h1>;
```

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

Elements are not components. They are what components are made of.

React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

### Sass

[Sass](https://sass-lang.com/) is a CSS extension language. "Sass" stands for syntactically awesome style sheets.

[Sassmeister](https://www.sassmeister.com/) is a playground for Sass. Add some Sass and SassMeister will show you the rendered CSS.



#### Additional Resources

[React - Hello World Example](https://reactjs.org/docs/hello-world.html)

[Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)

[Rendering Elements](https://reactjs.org/docs/rendering-elements.html)

[React cheatsheet](https://devhints.io/react)

[Another React cheatsheet](https://reactcheatsheet.com/)

[Sass](https://sass-lang.com/)

[Sassmeister](https://www.sassmeister.com/)

[Sass cheatsheet](https://devhints.io/sass)




---
[Home page](https://marlene-rinker.github.io/reading-notes/)