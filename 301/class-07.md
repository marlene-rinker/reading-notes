## Code 301 Reading Assignment Notes - Class 7

_May 12, 2020_

### Node.js

[What Google Learned About Teams](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html)

I read this in [201 Class 14](https://marlene-rinker.github.io/reading-notes/201/class-14). My key takeaway was that in the best teams, members listen to one another and show sensitivity to feelings and needs.

[How I Explained Rest to My Brother Article](https://gist.github.com/brookr/5977550)

Roy Fielding helped write the HTTP protocol that's used to get pages from servers to your browser.

It's capable of describing the location of something anywhere in the world from anywhere in the world. It's the foundation of the web. It's like GPS coordinates for knowledge and information.

"REST" is the architectural style that the whole world wide web is built on. 

A web page is a “representation” of a resource. Resources are just concepts. URLs tell the browser that there's a concept somewhere. A browser can then go ask for a specific representation of the concept. Specifically, the browser asks for the web page representation of the concept.

The basic concept behind APIs is that machines can use the web like people do. They use the same protocols to send messages back and forth to each other.

URLs are like nouns. "Polymorphism" is a geeky way of saying that nouns can have the same verb applied to them. Different kinds of nouns can be treated the same. You can use an HTTP GET to get an image, text, video, an mp3, slideshow, whatever, the same way if you have a URL.

Web browsers pretty much just get stuff. 

Machines just need the data. They don't care about layout and styling.

Retrieve information from another system: HTTP GET

Add information to another system: HTTP POST

Replace information in another system: HTTP PUT 

Partial update of information in another system: HTTP PATCH

[SuperAgent](https://visionmedia.github.io/superagent/) 

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js.

SuperAgent has two implementations: one for web browsers (using XHR) and one for Node.JS (using core http module). By default Browserify and WebPack will pick the browser version.

If want to use WebPack to compile code for Node.JS, you must specify node target in its configuration.

The article has lots of info and examples of how to use SuperAgent.



---
[Home page](https://marlene-rinker.github.io/reading-notes/)