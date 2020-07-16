## Code 401 Reading Assignment Notes - Class 29

_July 16, 2020_

[Routing](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-29/DISCUSSION)

#### Routing

Using `react-router`, you can easily toggle the visibility of components (or even pages) based on the URL/Route that the user engages with.

`import { Route } from 'react-router-dom';`

To use Browser Router properly, you eliminate your use of `<a>` tags and instead use it’s built-in `<Link>` component.

Example:

```
<Link to="/">Home</Link>
<Link to="/stuff">Stuff</Link>
```
In practice, then, use the router component to look at either `/` or `/stuff` and based on that, displaying either the `Home` or the `List` component.

```
<Route exact path="/" component={Home} />
 <Route exact path="/stuff" render={() => <List>{items}</List>} />
 ```

 **Component Composition - Logical**

 In this setup, you are sending your child components the raw data and allowing them to render the output as they decide.

 **Component Composition - Using Logic-less Children**

 This is typically used when your children are already in JSX form (pre-rendered) and you need to display them as a whole. A good example might be a gallery of images.

 [Today's Article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-29/DISCUSSION) has examples for logical and logic-less children component composition.



#### Additional Resources

[React Basics Recap](https://www.freecodecamp.org/news/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030/)

[React - props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)

[React Router Tutorial](https://blog.pshrmn.com/simple-react-router-v4-tutorial/)

[React - Composition vs Inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)

[React Router - API Docs](https://reactrouter.com/web/api)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)