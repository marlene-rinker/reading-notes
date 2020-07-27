## Code 401 Reading Assignment Notes - Class 37

_July 28, 2020_

### Redux - Combined Reducers

[Redux - Combined Reducers](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-37/DISCUSSION)

Combined reducers is nothing more than pulling in more than one reducer from source and creating a keyed object from them.

Once done, any component can reach into the store and get either one, both, or all.

Why would we do this?

- Obey the Single Responsibility Principle
  - Each reducer really should have only 1 part of state to manage
  - Is this more work/boilerplate? Yes.
  - Does it allow you decouple logic? Yes.

What about the actions?

- Each reducer technically has it’s own actions and creators.

- However, they can cross over and both be dispatched.

If two reducers have the same action, they will both respond so you have to be careful with this functionality.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-37/DISCUSSION) has some examples.





#### Additional Resources

[Multiple Reducers Video](https://www.youtube.com/watch?v=gBER4Or86hE)

[Redux - Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)

[Redux - Combined Reducers Syntax](https://redux.js.org/api/combinereducers/)




---
[Home page](https://marlene-rinker.github.io/reading-notes/)