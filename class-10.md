## Code 201 Reading Assignment Notes - Class 10

_April 10, 2020_

### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Error Handling and Debugging

_Ch. 10, “Error Handling & Debugging”_

The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks the new function on top of the current task.

Each time a new item is added to the stack, it creates a new execution context.

Variables defined in a function are only available in that function (or execution context). If the function is called a second time, the variables can have different values.

#### Writing from the script to the console

- console.log() - used for general information

- console.warn() - used for warnings

- console.error() - used to hold errors 

- console.group() - used to group messages together

```
console.group('Area calculation');
  console.info('Width ', width);
  console.info('Height', height);
  console.log(area);
console.groupEnd();
```
- console.table() - outputs a table showing objects and arrays that contain other objects or arrays

- console.assert() - test if a condition has been met and write to the console only if the expression evaluates to false

#### Breakpoints in Chrome

1. In Chrome, go to the dev tools Sources option. 

2. Select the script you are working with from the left-hand pane. The code appears to the right.
3. Find the line number you want to stop on and click it.
4. When you run the script it will stop on this line. You can now hover over any variable to see its value at that time in the script's execution.

(Can also put `debugger;` in the script to stop it at a certain point in your code.)

You can also enter conditional breakpoints by right-clicking on a line number, selecting **Add Conditional Breakpoint...**, and entering a condition in the popup box. When you run the script, it will only stop on this line if the condition is true.

#### Handling Exceptions

Use `try, catch, finally` statements to handle an error gracefully and give your users helpful feedback.

**Try**: specify the code you think might throw an exception

**Catch**: if the _try_ code block throws an exception, _catch_ steps in with an alternative set of code. It has one parameter - the error object.

**Finally**: the contents of the finally code block will run whether the try block succeeded or failed. 

```
try {
  // try to execute this code
} catch (exception){
  // if there is an exception, run this code
} finally {
  // this always gets executed
}
```

#### Throwing Errors

If you know something might cause a problem for your script, you can generate your own error messages before the interpreter creates them.

`throw new Error('message');`

---
[Home page](https://marlene-rinker.github.io/reading-notes/)