## Code 201 Reading Assignment Notes - Class 3

_April 1, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Lists
_Chapter 3: Lists (pp.62-73)_

There are three types of lists in HTML:
- **Ordered lists** - numbered list, used for steps in instructions

- **Unordered lists** - lists that begin with a bullet point

- **Definition lists** - lists of terms along with their definitions

### Boxes
_Chapter 13: Boxes (pp.300-329)_

CSS treats each element as if it's in its own box.

#### The Box Model

Every box has a **border**. 

You can use the `border` property as a shortcut to specify the width, style, and color of a border (in that order) in just one property.

**Padding** is the space between the border and the content inside the box.
Padding is most often specified in pixels.

You can use the `padding` property as a shortcut to specify the top, right, bottom, and left side padding (in that order) in just one property.



**Margin** is the space between the box and things outside of it.

If one box sits on top of another, margins are collapsed. This means the larger of the two margins will be used and the smaller will be disregarded.

You can use the `margin` property as a shortcut to specify the top, right, bottom, and left side margins (in that order) in just one property.


The display and visibility properties can be used to hide elements.



### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Decisions and Loops

_“Decisions and Loops” from switch statements on (pp.162-182)_

#### Switch statements

A switch statement starts with a switch value. Each case indicates a possible value for this variable and the code that should run if it matches.

There is also a `default` value that runs if none of the cases match.

The instructions for each case end with `break;` which tels JavaScript that it is finished with the switch statement and can move on to any subsequent code.

Example:

```
switch(level) {

  case 'One':
  title = 'Level 1';
  break;

  case 'Two':
  title = 'Level 2';
  break;

  default:
  title = 'Test';
  break;
}
```

#### Loops

Loops check a condition. If it returns true, a code block is run, then the condition is checked again. The code block will be run and the condition checked until the condition returns false.

**For Loops**

Use a for loop to run code a specific number of times. 

The condition is usually a counter which is used to tell how many times the loop should run.

**While Loops**

Use a while loop if you don't know how many times the code should run. The code will continue to run as long as the condition returns true.

**Do While Loops**

This is similar to the while loop except that it always runs the code at least once even if the condition is false.

The statements in the code block come before the condition.

**Other things**

`+=` operator is used to add new content to a variable


---
[Home page](https://marlene-rinker.github.io/reading-notes/)