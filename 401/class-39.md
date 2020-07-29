## Code 401 Reading Assignment Notes - Class 39

_July 30, 2020_

### Redux - Additional Topics

[Redux - Additional Topics](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-39/DISCUSSION)

#### Redux Toolkit

The makers of Redux made a Redux Toolkit which is a framework for making stores. It's an attempt to standardize the way you build stores so it will be familiar in different projects.

This toolkit specifies a few different means of building a reducer and action set that work well together and are easier to understand and integrate.

Example:
```javascript

const postsSlice = createSlice({ name: ‘posts’, initialState: [], reducers: { createPost(state, action) {}, updatePost(state, action) {}, deletePost(state, action) {} } })

// Extract the action creators object and the reducer const { actions, reducer } = postsSlice // Extract and export each action creator by name export const { createPost, updatePost, deletePost } = actions // Export the reducer, either as a default or named export export default reducer

// ————— Sample Use ————– // console.log(createPost({ id: 123, title: ‘Hello World’ })) // {type : “posts/createPost”, payload : {id : 123, title : “Hello World”}}

// Notice how createSlice transforms your defiition? console.log(postsSlice) /* { name: ‘posts’, actions : { createPost, updatePost, deletePost, }, reducer } */

```


#### Additional Resources

[Redux Toolkit](https://redux-toolkit.js.org/)

[Redux Toolkit Tutorial](https://redux-toolkit.js.org/tutorials/intermediate-tutorial)

[Ducks (modular redux)](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-39/DISCUSSION)

[MobX - state management solution](https://mobx.js.org/getting-started.html)

[Hookstate - state management solution](https://hookstate.js.org/)




---
[Home page](https://marlene-rinker.github.io/reading-notes/)