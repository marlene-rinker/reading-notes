## Code 301 Reading Assignment Notes - Class 2

_May 5, 2020_

### Pair Programming

[6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

Pair programming touches on four skills because developers: 

- explain out loud what the code should do (speaking)

- listen to others’ guidance (listening)

- read code that others have written (reading)

- write code themselves (writing)

The six benefits of pair programming are: 

1. Greater efficiency

2. Engaged collaboration

3. Learning from fellow students

4. Social skills

5. Job interview readiness

6. Work environment readiness



### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)


_pages 293-301, 306-331 and 354-357_

jQuery is a JavaScript file that you include in your web pages. It lets you find element using CSS selectors and then do something with the elements using jQuery methods.

It allows ou to achieve a variety of common JavaScript tasks quickly and consistently across browsers.

Use jQuery to select elements, perform tasks, and handle events.

Example of finding elements using CSS-style selectors: `$('li.hot')` where `li.hot` is the selector - `li` element with a class of `hot`. This creates a **jQuery object**.

Do something with the elements using **jQuery methods**.

Example: `$(li.hot).addClass('complete');` This adds a new value, `complete`, to the `class` attribute of the jQuery object `li.hot`.

jQuery makes coding simpler. "Write less, do more."

When you select one or more elements, a jQuery object is returned. This is also known as a matched set or a jQuery selection. Each element is given an index number.

jQuery methods both retrieve info from, and update the contents of, elements. They don't always apply to all elements.

`var content = $('li').html();` - returns the content of the first element in the matched set and stores it in a variable called `content`.

`$('li').html('Updated');` - this will update the content of each element in the matched set with the word "Updated."

A jQuery object stores references to elements. Cache a jQuery object to store a reference of it in a variable.

Example: `$('li');` stores the locations of the `<li>` elements in the DOM tree. `$listItems = $('li');` stores a reference to the object in a variable called `$listItems`. The `$` is used to differentiate it from other variables in your script.

jQuery's `.ready()` function checks that the page is ready for your code to work with. Shorthand for the ready function is 
```
$(function() {
  //your script goes here
});
```
**Including jQuery in your page**


You can try to load jQuery from a CDN (Content Delivery Network), then check to see if it loaded. If not, then you can include a version that's stored on your own servers as a fallback.

The position of the `<script>` elements can affect how quickly a page loads. The ideal location is before the closing `<body>` tag.

_pages 332-335_

Effects methods can enhance your web page with transitions and movement.
Page 332 has a list of basic effects and what they do.

You can create your own effects and animations by changing CSS properties with the `.animate()` method. You can animate any CSS property whose value can be represented with a number.

_pages 302-305_

Using jQuery, you usually select elements using CSS-style selectors. Pages 302 and 303 have a list of selectors and what they select. There are some extra selectors which are noted with a 'jQ'.

Pages 304 and 305 have a list of jQuery methods you can use to perform tasks on the elements that you select. If the jQuery selector doesn't find any results, the methods just won't do anything (you won't get an error).


---
[Home page](https://marlene-rinker.github.io/reading-notes/)