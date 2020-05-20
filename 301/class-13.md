## Code 301 Reading Assignment Notes - Class 13

_May 20, 2020_

### Sending Form Data

[Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)

#### What happens when a user submits a form?

The client sends a request to the server.

The `<form>` element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are `action` and `method`.

**Action**

The `action` attribute defines **where the data gets sent**. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.

**Method**

The `method` attribute defines **how data is sent**. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the `GET` method and the `POST` method.

The `GET` method is the method used by the browser to ask the server to send back a given resource. The data sent to the server is appended to the URL.

[Example of GET method](https://github.com/mdn/learning-area/blob/master/html/forms/sending-form-data/get-method.html)

`POST` is the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request. The data is appended to the body of the HTTP request.

[Example of POST method](https://github.com/mdn/learning-area/blob/master/html/forms/sending-form-data/post-method.html)

HTTP requests are never displayed to the user. You can see them after submitting the form by opening developer tools, going to Network, selecting All, selecting the URL in the Name tab, then selecting Headers.

Whichever HTTP method you choose, the server receives a string that will be parsed in order to get the data as a list of key/value pairs. The way you access this list depends on the development platform you use and on any specific frameworks you may be using with it. We're using Express for Node.js in class.

Sending files is a special case. Files are binary data, not text data, and therefore require special handling.

Each time you send data to a server, you need to consider security. Problems never come from the HTML forms themselves, they come from how the server handles data.

[Article about website security](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Website_security)

#### Resources

[Forms in HTML5](https://htmlreference.io/forms/) - this is a great resource for creating forms. It gives lots of examples - showing both the HTML and the result and explaining the options for creating the forms.

[Styling HTML5 Forms Video Series](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK) - this is a series of 6 videos that cover how to style forms.





---
[Home page](https://marlene-rinker.github.io/reading-notes/)
