## Reading Assignment Notes

_3/30/2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Introduction to HTML & CSS
_Introduction (pp.2-11)_

#### General terms
- _Web browser_: How you access a website. Examples: Firefox, Chrome, Safari
- _Web server_: Hosts the website
- _Devices_: what you are using to view the website
- _Screen reader_: for accessibility; reads content of the screen to you
- _ISP_: Internet Service Provider
- _DNS_: Domain Name System – a network of servers which acts like a phone book of IP addresses
- _IP address_: unique for each device on the web; like a telephone number for the computer, used to be 12 characters, but can now be up to 32 characters

#### How the web works
1. You connect to the web through an ISP. To visit a site, type a domain name or website address into your browser.

2.  Your computer contacts the DNS which sends back the IP address for the domain name you entered.

3. Your browser uses the IP address to contact the web server which hosts the website.

4. The web server sends the page you requested back to your browser.




### Structure
_HTML Chapter 1: “Structure” (pp.12-39)_

HTML describes the structure of the pages. It makes the information easier to understand.

**Elements**

- Elements tell the browser about the information between the opening and closing tags. These tags are like containers for the information.

- Example of an element: `<p>This is a paragraph.</p>`. The character between the brackets indicates the tag’s purpose which in this case is a paragraph.

**Attributes**

- Attributes provide additional info about the contents of an element.

- Attributes are made up of a name and a value separated by an equals sign.

- Example of an attribute: `<p lang=”en-us”>This is a paragraph in US English.</p>`.

Most attributes can only be used with certain elements. The attribute values are either pre-defined or follow a set format.

**Body, Head, and Title Elements**

`<body>` - everything inside this tag is shown in the main browser window

`<head>` - comes before the body tag – contains info about the page, rather than what’s on the page; `<title>` is usually in `<head>`

`<title>` - contents of this element are shown in the top of the browser or on the tab for the page, depending on your browser

**View Source**: Use this to view the source code that made up a website. Right click on a page and choose View Page Source. Can also choose Inspect.

To learn HTML, you need to know what tags are available, what they do, and where they can go.




### Extra Markup

_HTML Chapter 8: “Extra Markup” (p.176-199)_

There are different versions of HTML. HTML5 is the newest version, but it’s not complete and isn’t supported by all browsers. HTML 4 was released in 1997. XHTML 1.0 was released in 2000.

Because there are different versions of HTML, each webpage should begin with a DOCTYPE that tells the browser which version of HTML the page is using. Example: `<!DOCTYPE html>` is for HTML5.

Comments aren’t visible on the page. They are used to make the code easier to understand or to stop certain code from being displayed.
`<! - - This is a comment - - >`

**ID attribute**

Uniquely identifies an element from other elements on the page. 

Should only be used on one element on the page. 

Should start with a letter or underscore. 

Allows you to style the element in a different way than other instances of the same element on the page. 

Example: `<p id=”ordernumber”>1234</p>`

**Class attribute**

Used to identify several elements that are different from other elements on the same page.
Example: `<p class=”warning”>Be careful!</p>`

Can assign multiple classes to the same element; separate the class attributes with a space
Example: `<p class=”warning important”>Be very careful!</p>`

**Block elements and Inline elements**

Block elements always appear to start on a new line in the browser. Examples: `<h1>`, `<p>`, `<ul>`, and `<li>`

Inline elements always appear to continue on the same line as neighboring elements in the browser. Examples: `<a>`, `<b>`, `<em>`, and `<img>`

**More elements**

Use the `<div>` element to group a set of elements together in a block.

The `<span>` element is used inline. It can be used to differentiate the content from surrounding text or contain a number of inline elements. 

The `<iframe>` element is like a window on your page where you can see another page. A common example is embedding a Google Map on a page.

The `<meta>` element lives inside the `<head>` element. It contains info about the page such as telling search engines about the page, who wrote the page, if the page is time sensitive, and more.

**Escape characters**

Use escape characters to display characters on your page that are used in HTML. For example, use `&lt;` to display the left angle bracket. 

[List of escape characters](http://www.htmlandcssbook.com/extras/html-escape-codes/)


### HTML5 Layout

_HTML Chapter 17: “HTML5 Layout” (pp.428-451)_

Many `<div>` elements from traditional HTML have been replaced with new elements with names that are based on the type of content. 

Traditional HTML: `<div id=”header”>` vs HTML5 `<header>`

**Examples**

`<header>` -can be used at the top of every page, in an individual article, or in an individual section on the page

`<footer>`-can be used at the bottom of every page, in an individual article, or in an individual section on the page

`<nav>` - contains navigation blocks on the site such as the primary site navigation

`<article>` - container for any section of the page that could stand alone

`<aside>` - inside an article; contains info that’s related to the article, but not essential; outside an article: contains content related to the entire page

`<section>` - groups related content together, should have its own heading

`<hgroup>` - groups a set of one or more `<h1>` through `<h6>` elements together to form a single heading

`<figure>` - used for content that’s referenced from the main flow of an article; examples include images, videos, graphs, diagrams, code samples, text that supports the main body of the article; the article should still make sense if the content of the `<figure>` is removed.

`<figcaption>` - should be used within the `<figure>` element to provide a text description of the content

`<div>` - used to group elements together; still needed when there is no suitable element to group a set of elements

**Older browsers**

Older browsers may not understand HTML5 and need to be told which elements are block elements. Example CSS for this: 
```
header, section, footer, aside, nav, article, figure, figcaption {
Display: block;
}
```

Extra JavaScript (available free from Google) is needed to make HTML5 elements work in IE 8 and older versions.


### Process & Design

_HTML Chapter 18: “Process & Design” (pp.452-475)_

Gather information you need to determine what needs to go on your site

- Who is the site for? Target audience

- Why are people coming to your site? Understand their key motivations and specific goals

- What are your visitors trying to achieve? Key tasks and motivations

- What information do your visitors need? Key info needed to achieve their goals quickly and effectively

- How often will people visit your site? Influences how frequently info needs to be updated

Once you know what needs to go on your site, organize the info into sections or pages.

_Site map_: a diagram of the pages that will be used to structure the site

Create a wireframe to sketch out how the information will be displayed on the page.

**Keep in mind** 

_Visual Hierarchy_ – order in which your eyes perceive what they see; it’s created by adding visual contrast between the items being displayed. Done using size, color, style, and images.

_Group related info together_ to make the design easier to comprehend.

_Navigation_ helps people find where they want to go, and also understand what your site is about and how it is organized.



### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)


### Introduction to JavaScript
_Introduction_

JavaScript makes a webpage feel more interactive. It responds to what a user does. It can be used to: 

- **Access** the content of the page

- **Modify** the content of the page

- **Program** rules or instructions the browser can follow

- **React** to events triggered by the user or browser



### The ABC of Programming

_JS Chapter 1: “The ABC of Programming” (pp.11-52)_

**Scripts**

Scripts are a series of step-by-step instructions that a computer can follow.

To write a script, you need to know your goal and the list of tasks that need to be completed to achieve it.

1. Define the goal.
2. Design the script.
3. Code each step.

Flowchart the tasks, then break each task down into the list of steps to complete the task. These steps can then be translated into individual lines of code.

Computers solve problems programmatically – following a series of instructions, one after another.

**Models**

Computers create models of the world using data.

**Objects (Things)** – each object can have its own _properties_, _events_, and _methods_, these create a working model of that object

- **Properties (Characteristics)** – each property has a name and a value that tells you something about that individual object

- **Events** are common ways people interact with the object. An event says that something just happened. Events can trigger specific sections of code.

- **Methods** represent what people need to do with objects. They can retrieve or update the values of an object’s properties. The code for a method can contain lots of instructions that together represent one task.

Web browsers are programs built using objects. 

- Window object – browser window

- Document object – web page loaded on the browser window

**Creating web pages**

Three languages used to create web pages. When possible, keep these languages in separate files with the HTML page linking to the CSS and JavaScript files.

- **HTML** – content layer; gives the page structure, where the content lives

- **CSS** – presentation layer; rules for how the content is presented

- **JavaScript** – behavior layer; adds interactivity to the page

This approach is called _progressive enhancement_.


**Using JavaScript**

To use JavaScript with a web page, use the `<script>` element. The `src` attribute tells people where to JavaScript file is stored. Example `<script src=js/add-content.js”></script>`

Although you can put JavaScript directly into a page between opening `<script>` and closing `</script>` tags, it’s best to put scripts in their own files.

Example line of JavaScript that shows how to use objects and methods also known as calling a method of an object:
 `document.write(‘Good afternoon! ‘);`

`document` = Object

`.` = Member Operator

`write()` = Method which allows new content to be written on the page where the `<script>` element sits

`‘Good afternoon! ‘` = Parameters – information the method requires in order to work; in this case, the write() method needs to know what to write on the page

JavaScript runs where it’s found in the HTML. When the browser gets to a `<script>` element, it loads the script and then checks to see if it needs to do anything.

JavaScript doesn’t change the HTML.

---
[Home page](https://marlene-rinker.github.io/reading-notes/)