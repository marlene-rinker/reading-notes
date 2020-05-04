## Code 301 Reading Assignment Notes - Class 1

_May 4, 2020_

### Responsive Web Design

[Shay Howe's Intro to Responsive Web Design](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

Responsive Web Design is the practice of building websites to work on all devices and screen sizes.

Responsive web design is broken down into three main components: 

- flexible layouts

- media queries

- flexible media

#### Flexible Layouts

Flexible layouts do not advocate the use of fixed measurement units, such as pixels or inches. There's a formula to help identify the proportions of a flexible layout using relative values

The formula is based around taking the target width of an element and dividing it by the width of it’s parent element. The result is the relative width of the target element.

#### Media Queries

Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example.

The best way to initiate media queries is with an `@media` rule inside an existing stylesheet. Other ways are to have a separate stylesheet or using an `@import` rule.

Each media query may include a **media type** followed by one or more expressions. Common media types include `all`, `screen`, `print`, `tv`, and `braille`. `screen` is the default media type if one isn't specified.

There are three different **logical operators** available for use within media queries: `and`, `not`, and `only`.

When using the `not` and `only` logical operators the media type may be left off. In this case the media type defaults to `all`.

**Media features** identify what attributes or properties will be targeted within the media query expression.

_**Height and Width**_

Within responsive design the most commonly used features include `min-width` and `max-width`. 

_**Orientation**_

The orientation media feature determines if a device is in the `landscape` or `portrait` orientation.

The `aspect-ratio` and `device-aspect-ratio` features specifies the `width/height` pixel ratio of the targeted rendering area or output device. 

The value for the aspect ratio feature consist of two positive integers separated by a forward slash. The first integer identifies the width in pixels while the second integer identifies the height in pixels.

_**Resolution**_

The `resolution` media feature specifies the resolution of the output device in pixel density, also known as dots per inch or DPI.This can also be specified in dots per pixel (1.3dppx), dots per centimeter (118dpcm), and other length based resolution values.

_**Other Media Features**_

Other less commonly used media features include identifying available output colors with use of the `color`, `color-index`, and `monochrome` features, identifying bitmap devices with the `grid` feature, and identifying the scanning process of a television with the `scan` feature.

Media queries don't work in IE8 and below.

It's a bad idea to write media query breakpoints around common viewport sizes as determined by different device resolutions, such as 320px, 480px, 768px, 1024px, 1224px, and so forth. 

_**Mobile First**_

This is a popular technique that designs for smaller screens by default.

_**Viewport**_

The `viewport` meta tag is used to identify the viewport size, scale, and resolution of a website.

Example: `<meta name="viewport" content="width=device-width, initial-scale=1">`

It's been recommended to move the `viewport` meta tag to a CSS rule `@viewport` instead. This isn't supported by many browsers yet. 

Example:

```
@viewport {

  width: device-width;

  zoom: 1;

}
```

#### Flexible Media

Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

One quick way to make media scalable is by using the `max-width` property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.

The `max-width` property doesn’t work well for all instances of media, specifically around `iframes` and embedded media. 

The article has details about a workaround for this issue.

### Floats

[All about Floats article](https://css-tricks.com/all-about-floats/)

This article is a great resource for understanding floats and how to use them.

**Float** is a CSS positioning property. Floated elements are part of the flow of the webpage. Other elements flow around them. This is different from Absolute positioned elements. Those elements are removed from the flow of the webpage.

Values are: Left, Right, None, and Inherit

Floats can be used for the layout of the entire webpage, although there are tools like Flexbox and Grid that are better to use. Floats still come in handy for small parts of webpages.

Float's sister property is `clear`. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.

Values are: Both, Left, Right, and None

Collapsing almost always needs to be dealt with to prevent strange layout and cross-browser problems. We fix it by clearing the float after the floated elements in the container but before the close of the container.

The article contains different ways to clear the float and to address problems with the float.

### CSS Resources

[Don't Overthink It Grids](https://css-tricks.com/dont-overthink-it-grids/) - good for simple grids - Flexbox or Grids is easier way to do this for larger grids; it has a link to a good CodePen demo

[CSS floats explained by riding an escalator](https://www.freecodecamp.org/news/css-floats-explained-by-riding-an-escalator-57fa55232333/)

[Scalable and Modular Architecture for CSS](http://smacss.com/) - guide to structuring your CSS to allow for flexibility and maintainability as your project and your team grows



---
[Home page](https://marlene-rinker.github.io/reading-notes/)