## Code 201 Reading Assignment Notes - Class 11

_April 13, 2020_

### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Images
_Chapter 16: “Images” (pp.406-427)_

Use CSS to specify dimensions of images. This is helpful when you want to use the same sized images on several pages of your site.

You can also use CSS to align images horizontally and vertically.

You can put a background-image behind the box created by any element on the page. You can also repeat the image across the background of the box instead of just showing it once.

By moving the background position of an image, you can create image roll-over effects.

Create image sprites to reduce the number of images your browser has to load. A sprite is a single image that is used for several different parts of an interface. For example, you could add the logo, other interface elements, and buttons to an image.

### Practical Information
_Chapter 19: “Practical Information” (476-492)_

Search engine optimization (SEO) helps visitors find your site when using search engines.

Keywords and phrases, location of content on the page, and links to other pages can affect SEO.

You can use [Google Analytics](www.google.com/analytics) for free to find out how visitors find your site, what they're looking at, and at what point they leave.

To put your site on the web, you need to get a domain name and web hosting. There are fees for this. Many sites that offer domain name registration also offer web hosting.

There are a number of online services that allow you to point your domain name to their servers. If you're using one of these platforms, you won't need your own hosting for the website, but you may need hosting for your email. Some web hosting companies offer packages that will just offer email services.

Examples of these platforms include Shopify (e-commerce) and WordPress (blogging). This saves you from having to write these platforms yourself.

You can transfer files from your local computer to your webserver using FTP programs.

### MDN Article on audio and video elements
[Video and Audio APIs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)

HTML5 comes with elements for embedding rich media in documents - `<video>` and `<audio>`

The `HTMLMediaElement` API provides features to allow you to control video and audio players programmatically.

Can use icon fonts instead of images. The `@font-face` block imports a custom web font, which is an icon font. Then the icon font is used for the button, instead of an image.
```
@font-face {
   font-family: 'HeydingsControlsRegular';
   src: url('fonts/heydings_controls-webfont.eot');
   src: url('fonts/heydings_controls-webfont.eot?#iefix') format('embedded-opentype'),
        url('fonts/heydings_controls-webfont.woff') format('woff'),
        url('fonts/heydings_controls-webfont.ttf') format('truetype');
   font-weight: normal;
   font-style: normal;
}
button:before {
  font-family: HeydingsControlsRegular;
  font-size: 20px;
  position: relative;
  content: attr(data-icon);
  color: #aaa;
  text-shadow: 1px 1px 0px black;
}
```
Use HTML and CSS to set up the interface and then JavaScript to get the buttons and controls working.


---
[Home page](https://marlene-rinker.github.io/reading-notes/)