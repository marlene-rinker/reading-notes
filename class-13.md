## Code 201 Reading Assignment Notes - Class 13

_April 15, 2020_

### Local Storage for Web Applications
[The Past, Present, and Future of Local Storage for Web Applications](http://diveinto.html5doctor.com/storage.html)

#### Cookies
Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:

- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over

- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)

- Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful

#### History
Over the years, people and big companies have come up with different solutions. However, all of them are either specific to a single browser, or reliant on a third-party plugin. 

They all expose radically different interfaces, have different storage limitations, and present different user experiences.

#### HTML5 Storage

HTML5 set out to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.

HTML5 Storage is a way for web pages to store named key/value pairs locally, within the client web browser. 

- Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. 

- Unlike cookies, this data is never transmitted to the remote web server (unless you go out of your way to send it manually).

From your JavaScript code, you’ll access HTML5 Storage through the localStorage object on the global window object.

It's important to check if the browser supports HTML5 Storage. You can do this using [Modernizer](http://diveinto.html5doctor.com/detect.html#modernizr) so you don't have to write the function yourself.

```
if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```
HTML5 Storage is based on named key/value pairs. 

- You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. 

- The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. 
- If you are storing and retrieving anything other than strings, you will need to use functions like `parseInt()` or `parseFloat()` to coerce your retrieved data into the expected JavaScript datatype.

The Using HTML5 Storage section of the article lists the syntax for different things you can do in HTML5 Storage.

**Tracking HTML5 Storage**
If you want to keep track programmatically of when the storage area changes, you can add an event listener. The storage event is fired on the window object whenever `setItem()`, `removeItem()`, or `clear()` is called and _actually changes something_. 

The storage event is supported everywhere the `localStorage` object is supported.

`handle_storage` will be called with the `StorageEvent` object, except in IE where the event object is stored in `window.event`.

The storage event is not cancelable. From within the `handle_storage` callback function, there is no way to stop the change from occurring. It’s simply a way for the browser to tell you the change happened.

Limitations of HTML5 Storage
- 5MB of storage is the default for each origin

- `QUOTA_EXCEEDED_ERR` is the exception that gets thrown if you exceed your storage quota of 5 megabytes. 

- You can't ask the user for more storage space.

The HTML5 Storage in Action section provides an example of using it for a game application.

There are competing visions of what HTML5 Storage may be like in the future. 

---
[Home page](https://marlene-rinker.github.io/reading-notes/)