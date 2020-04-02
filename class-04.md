## Code 201 Reading Assignment Notes - Class 4

_April 2, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Links
_Chapter 4: Ch.4 “Links” (pp.74-93)_

Links are created using the `<a>` tag. `href` specifies the page to link to. 

You should use words that people might use when searching for that page when writing the link text.

`<a href="http://www.imdb.com">IMDB</a>` - contains the link to the page www.imdb.com and the text you click on "IMDB" to go to the website.

Use relative links to link to other pages on your own site, instead of qualified URLs.

Use the id element to target elements on the page that can be linked to.


### Layout
_Chapter 15: “Layout” (pp.358-404)_

_Focus your attention on understanding the core concepts presented on pp.358-364, and look at the code samples on the website that accompanies the textbook._

CSS treats each HTML element as if it's in its own box.

Block-level elements - start on a new line, `<h1>`, `,<p>`, `<ul>`, `<li>`

Inline elements - flow in between the surrounding text `<img>`, `<b>`, `<i>`

If a block level element sits inside another block level element, the outer box is known as the containing or parent element.

#### Positioning
**Normal flow** - default, each block level element is on a new line, moving down the page

**Relative positioning** - moves element from its normal position; surrounding elements don't move

**Absolute positioning** - positions the element in relation to its containing element. It doesn't affect the position of surrounding elements. These elements move as users scroll up and down the page.

**Fixed positioning** - form of absolute positioning; positions the element in relation to the browser window; doesn't affect the position of surrounding elements

**Floating positioning** - positions an element to the far left or far right of a containing box. The floated element becomes a block-level element around which other content can flow.

If boxes overlap, the `z-index` property controls which box appears on top.

#### Screens

Consider screen size (devices have different sized screens) and screen resolution (number of dots shown per inch) when designing your site.

Fixed width layout - doesn't change size when a user resizes their browser window; measurements tend to be given in pixels

Liquid layout - stretch and contracts ans the user resizes their browser window; they tend to use percentages.


### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Functions, Methods, and Objects

_Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)_

#### Functions

**Declaring a Function**

```
function sayHello() {
  document.write('Hello');
}
```
`function` is the function keyword.

`sayHello()` is the function name.

`{document.write('Hello');}` is the code block.

Use functions for tasks you perform multiple times.

Most functions have multiple statements.

**Calling a Function**

`sayHello();` - call the function using it's name. this runs the statements in the code block.


**Declaring functions that need information**

```
function getArea(width, height) {
  return width * height;
}
```

Parameters go in the parenthesis; they're used like variables within the function.

**Calling functions that need information**


`getArea(3, 5);` - arguments as values

```
wallWidth = 3;
wallHeight = 5;
getArea(wallWidth, wallHeight);//arguments as variables
```

**Get a single value out of a function**

```
function calculateArea(width, height) {
  var area = width * height;
  return area;
}
var wallOne = calculateArea(3, 5);
var wallTwo = calculateArea(8, 5);
```
Function returns information to the code In this case, a single value - the area calculation result.

***Get multiple values out of a function***

```
function getSize(width, height, depth) [
  var area = width * height;
  var volume = width * height * depth;
  var sizes = [area, volume];
  return sizes;
]
var areaOne = getSize(3, 2, 3)[0];
var volumeOne = getSize(3, 2, 3)[1];
```

Functions can return more than one value using an array. In this case, the array is `sizes` and it contains the area and volume values.


### Code Fellows Pair Programming Article
[6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

In pair programming, two developers share a single workstation and work on a coding task together. This is common in many agile work environments.

One person is the Driver and the other is the Navigator.

Driver - types and manages the code

Navigator - looks at the big picture, does research on their computer, looks for bugs and typos, doesn't write any code


---
[Home page](https://marlene-rinker.github.io/reading-notes/)