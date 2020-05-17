## Code 301 Reading Assignment Notes - Class 11

_May 18, 2020_

### EJS - Embedded JavaScript

[EJS Tutorials](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt) - watched 1 - 5 for class

#1 was an overview of the tutorial series.

#### Getting Started (#2)

run `npm init -y`

run `npm install --save express body-parser cors ejs`

Then the tutorial goes through how to set up server.js.

Uses "path" which doesn't have to be installed. It is a built-in module for node. It takes two paths and it joins them.

John shows and explains how he sets up the server.

#### Inject values into the view (#3)

John explains response.render().

`<%= foo %>` syntax for where to insert value in .ejs file from the .js file

John shows how to inject a value into a route in a render of page.

### For Loops and Arrays (#4)

John shows how to iterate over an array value.

He shows the syntax to put on the .esj file and what to put in the .js file. He creates an array of objects in the .js file and puts the name value from each object in a list on the page in the .ejs file.

### If/Else statement (#5)

John shows how to use an if/else statement in the .ejs file.

He uses the same info in the .js file from #4.

`<%  %>` - code on each line goes in between these.

### Google Books API

[Google Books API Docs](https://developers.google.com/books/docs/v1/using#WorkingVolumes) - reviewed the Working with Volumes section for class

Note: Performing a search does not require authentication, so you do not have to provide the Authorization HTTP header with the GET request. However, if the call is made with authentication, each Volume will include user-specific information, such as purchased status.

Installed [Postman](https://learning.postman.com/getting-started/) and made some API calls to the Google Books API.


#### References

[EJS](https://ejs.co/) - embedded JavaScript reference guide

[EJS tutorial](https://scotch.io/tutorials/use-ejs-to-template-your-node-application) - this is a tutorial for templating with EJS

[Source Code from EJS tutorial](https://github.com/scotch-io/node-ejs) - this is the source code for the EJS tutorial


---
[Home page](https://marlene-rinker.github.io/reading-notes/)