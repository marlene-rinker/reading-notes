## Code 201 Reading Assignment Notes - Class 9

_April 9, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Forms
_Chapter 7: “Forms” (p.144-175)_

Forms allow users to perform functions online such as search, adding text, making choices, submitting forms, and uploading files.

To collect information from visitors, you need a form, which lives inside a `<form>` element.

#### How forms work

1. A user fills in a form and then presses a button to submit the information to the server.
2. The name of each form control is sent ot the server along with the value the user enters or selects.
3. The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.
4. The server creates a new page to send back to the browser based on the information received.

A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element.

To differentiate between various pieces of inputted data, information is sent from the browser to the server using name/value pairs.

Example: `username=Ivy` where `username` is the name and `Ivy` is the value.

You should never change the name of a form control in a page unless you know that the code on the server will understand this new value.



### Lists, Tables & Forms
_Chapter 14: “Lists, Tables & Forms” (pp.330-357)_

Some CSS properties are specifically used to control the appearance of lists, tables, and forms.

There are properties you can use to control borders and spacing of table cells to make them more consistent in different browsers.

Forms are easier to use if the form controls are vertically aligned using CSS.

Form styles can make them feel more interactive.



### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Events

_Chapter 6: “Events” (pp.243-292)_

#### How JavaScript triggers code

When the user interacts with the HTML on a web page, there are three steps involved in getting it to trigger some JavaScript code.

1. **Select Element** - Select the element node(s) you want the script to respond to.
2. **Specify Event** - Indicate which event on the selected node(s) will trigger the response. (This is known as binding an event to a DOM node.)
3. **Call Code** - State the code you want to run when the event occurs.


#### Ways to bind an event to an element

- HTML Event Handler - this is a bad practice; don't do this; be aware of it because you may see it in older code.

- Traditional DOM event handlers - separates the JavaScript from the HTML, supported by most browsers, you can only attach a single function to any event with this method, if more than one script is used on a page and both scripts respond to the same event, then one or both of the scripts may not work as intended

- DOM Level 2 event listeners - this is now the favored way of handling events, it allows one event to trigger multiple functions, less likely to have conflicts between different scripts that run on the same page


#### Event flow

HTML elements nest inside other elements. If you hover or click on a link, you will also be hovering or clicking on its parent elements.

Event bubbling - the event starts at the most specific node and flows outwards to the least specific one. This is the default type of event flow with wide browser support.

Event capturing - the event starts at the least specific node and flows inwards to the most specific one. This is not supported in Internet Explorer 8 and earlier.

#### Why flow matters

The flow of events only really matters when your code has event handlers on an element and one of its ancestor or descendant elements.

Event handlers default to using event bubbling. 

Event listeners have a final parameter in the `addEventListener()` method that lets you choose the direction to trigger events. 

- `true` = capturing phase
- `false` = bubbling phase (this is often a default choice since capturing is not supported in IE 8 or earlier)

#### Where events occur

The `event` object can tell you where the cursor was positioned when an event was triggered.

- Screen - `screenX` and `screenY` properties indicate the position of the cursor within the entire screen on your monitor, measuring from the top left corner of the screen (rather than the browser)
- Page - `pageX` and `pageY` properties indicate the position of the cursor within the entire page. 
- Client - `clientX` and `clientY` properties indicate the position of the cursor within the browsers viewport


---
[Home page](https://marlene-rinker.github.io/reading-notes/)