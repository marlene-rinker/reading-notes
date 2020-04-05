### Simple Programmer Article
[Understanding the Problem Domain is the Hardest Part of Programming](https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming)

Writing code is a lot like putting together a jigsaw puzzle.

Programming is easy if you understand the problem domain. Waterfall development was easier because you got a spec with all of the details so it was easy to understand the problem domain. It can be harder to understand the problem domain in Agile development.

Understanding the problem is the most critical piece to the equation. It is very difficult to solve a problem before you know the question.

### How to make programming easier
Do one of these two things to make programming easier.

**Make the problem domain easier**

Cut out cases and narrow your focus to a particular part of the problem. Make sure you understand a part of the problem before expanding the problem domain.

**Get better at understanding problem domains**

Talk to other people - customers, product manager, user experience designer - to make sure you understand the problem inside and out before you try to solve the problem with code.

### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Object Literals

_Chapter 3: “Object Literals” (pp.100-105)_

Objects group together a set of variables and functions to create a model of something you would recognize in the real world. In an object, a variable is known as a property and a function is known as a method.

#### Creating an object: literal notation

```
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function(){
    return this.rooms - this.booked;
  }
}
```
`hotel` is the object.

`name: 'Quay',
  rooms: 40,
  booked: 25,` are the properties.

  `checkAvailability: function(){
    return this.rooms - this.booked;
  }` is the method.

  In the `checkAvailability()` method, the `this` keyword means that the `rooms` and `booked` properties come from this object.

#### Accessing an object and dot notation

Access the properties and methods of an object using dot notation.

```
var hotelName = hotel.name;
var roomsFree = hotel.checkAvailability();
```

`hotel` is the object.

the dot `.` is the member operator.

`name` is the property name.

`checkAvailabilty()` is the method name.

You can also access the properties of an object, but not its methods using the square brackets.

`var hotelName = hotel['name'];` - the object name is followed by square brackets with the property name inside them. This is commonly used when the name of the property is a number (not recommended) or a variable is being used in place of the property name.

### Document Object Model

_Chapter 5: “Document Object Model” (pp.183-242)_

The **Document Object Model (DOM)** specifies how browsers should crete a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.

The DOM is an API (Application Program Interface).

The DOM tree is the model of the web page. It consists of four main types of nodes. Each node is an object with methods and properties.

- Document Node - represents the entire page
- Element Nodes - describe the structure of the page
- Attribute Nodes - part of the elements that carry them; can be changed by JavaScript
- Text Nodes - text within an element

To work with the DOM tree:

1. Access the elements - locate the node that represents the element you want to work with
2. Work with those elements - use its text content, child elements, and attributes

DOM queries - methods that find elements in the DOM tree


`getElementByID('one');` - this gets the _**location**_ of an element with the ID of 'one'

`var itemOne = getElementByID('one');` - use a variable to store the location of the element if you plan to use it more than once; this is called "caching the selection" and improves performance since the browser only has to look for the element once. Syntax: the variable stores a reference to the object in the DOM tree.

#### Methods that select individual elements

`getElementByID()` and `querySelector()` search the entire element and return individual elements. They use similar syntax.

`getElementByID()` is the quickest and most efficient way to access an element because no two elements can share the same value for their id attribute.

`querySelector()` isn't supported by older browsers. It's very flexible because its parameter is a CSS selector which means it can be used to accurately target many more elements.

`document.getElementByID('one');` 

`document` is the object.

`.` is the member operator.

`getElementByID('one')` is the method.

`'one'` is the parameter.

#### Selecting elements from a NodeList

Whenever a DOM query can return more than one node, it will always return a NodeList.

A NodeList is a collection of element nodes. Each node is given an index number like an array. 

The order in which the element nodes are stored in a NodeList is the same order that they appeared in the HTML page.

An element node can contain multiple text modes and child elements that are siblings of each other.

From an element node, you can access and update content using properties such as textContent and innerHTML or using DOM manipulation techniques.

**The item() Method**

Returns an individual node from the NodeList. 

You specify the index number of the element you want as a parameter of the method. 

It's a good practice to make sure there is something in the NodeList before running any code.

```
var elements = document.getElementByClassName('hot')
if (elements.length >= 1) {
  var firstItem = elements.item(0);
}
```
In this example, we:

1. Select elements with a class attribute that has a value of 'hot' and store the NodeList in a variable called elements. 

2. Then we use the length property to check how many elements are found, and run the code in the if statement if 1 or more are found. 

3. If one or more are found, store the value of the first element from the NodeList in a variable called firstItem.

**Array Syntax**

This is preferred over the item() method because it's faster. 

Before selecting a node from a NodeList, check that it contains nodes. If you repeatedly use the NodeList, store it in a variable.

```
var elements = document.getElementsByClassName('hot');
if (elements.length >=1 {
  var firstItem = elements[0];
}
```
In this example we:

1. Create a NodeList containing elements that have a class attribute whose value is hot and store it in a variable called elements.

2. If there are 1 or more elements in the NodeList, run the code in the if statement.

3. Get the first element from the NodeList and store it in a variable called firstItem.

#### Repeating actions for an entire NodeList

When you have a NodeList,, you can loop through each node in the collection and apply the same statements to each.

Here's an example using a for loop to go through a NodeList stored in the variable hotItems. It changes the value of the class attribute from 'hot' to 'cool'.

```
var hotItems = document.querySelectorAll('li.hot');
for (var i =0; i < hotItems.length; i++) {
  hotItems[i].className = 'cool';
}
```
#### Adding or removing HTML content

**The innerHTML Property**

There are security risks to this approach.

It can be used on any element node to retrieve and replace content.

To update an element, new content is stored as a string in a variable (`var item; item = '<em>Fresh</em> figs';`). Then you select the element whose content you want to replace and set the elements innerHTML property to be the new string. 

To remove all content from an element, you set innerHTML to an empty string.

_`textContent` is another property you can use that is similar.

**DOM Manipulation Property**

It can be sager than innerHTML, but requires more code and can be slower.

To add content you use a DOM method to create new content one node at a time and store it in a variable. Then another DOM method is used to attach it to the right place in the DOM tree.

You can remove an element along with its content and any child elements from the DOM tree using a single method.

#### Attribute nodes

Once you have an element node, you can use other properties and methods on that element node to access and change its attributes.

Steps:

1. Select the element node that carries the attribute

2. Use one of these methods or properties to work with that element's attributes:
    
    Methods

    - `getAttribute()`  - gets the value of an attribute

    - `hasAttribute()` - checks if element node has a specified attribute

    - `setAttribute()` - sets the value of an attribute

    - `removeAttribute()` - removes an attribute from an element mode

    Properties

    - `className`  - gets or sets the value of the **class** attribute

    - `id` - checks if element node has a specified attribute

    - The properties of the object correspond to the attributes that type of element can carry. Other properties are `accessKey`, `checked`, `href`, `lang`, and `title`.

    
Example:

`document.getElementByID('one').getAttribute('class');`

`document.getElementByID('one')` is the DOM Query; it finds the element node

`.` is the member operator.

`getAttribute('class')` is the method; it gets the value of the attribute that was give as a parameter of the method


#### Viewing the DOM tree

Browsers have tools for viewing the DOM tree.

In Chrome, go to the developer tools and inspect the element. See page 236 in the book for more details.


---
[Home page](https://marlene-rinker.github.io/reading-notes/)