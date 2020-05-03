## Code 201 Reading Assignment Notes - Class 8

_April 8, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)

**Today's reading assignment is a repeat of part of the Class 4 assignment.**

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


---
[Home page](https://marlene-rinker.github.io/reading-notes/)