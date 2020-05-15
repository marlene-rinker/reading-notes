## Code 301 Reading Assignment Notes - Class 10

_May 15, 2020_

### The Call Stack

[The Call Stack - MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)

A call stack is a way for an interpreter (such as the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions.

- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

In summary, then, we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.

[Understanding the JavaScript Call Stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accommodate before throwing a stack error.

The key takeaways from the call stack are:
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

[JavaScript Error Messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

**Reference errors** - You get these when you try to use a variable that isn't declared yet. 

**Syntax errors** - This occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using `JSON.parse`. You could also get this error for something like sending a trailing comma when calling a function.

**Range errors** - This happens when you try to manipulate an object with some kind of length and you give it an invalid length.

**Type errors** - This happens when the types (number, string, etc.) you are trying to use or access are incompatible, like access a property in an _undefined_ type of variable.

#### Debugging

To debug your JS code, the easiest and maybe the most common way its to simply `console.log()` the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).

If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting.
The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values.

You can see the stack trace at any given point in your code by just writing console.trace() were you want to log it.

#### Handling Errors

We usually **try** to **catch** the errors so we can gracefully fallback to a default state of our application in case of an error.

```
try {
      var result = a + b
      return result.split('')
    } catch (error) {
      console.error('add went wrong ->', error)
      return [] // default value
    }
```

JavaScript is not a compiled language like Java so your errors will happen at runtime, that means that you can only see whatever is wrong with your code after your run it.

Some tools to help avoid runtime errors are:

- [quokka](https://quokkajs.com/) to evaluate your code as you type

- [eslint](https://eslint.org/) to make sure your style guide is consistency and it will grab you an error or two along the way

[JavaScript Error Reference from MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors) - this is a list of errors and how to fix them for reference


---
[Home page](https://marlene-rinker.github.io/reading-notes/)