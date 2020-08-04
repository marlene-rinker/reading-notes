## Code 401 Reading Assignment Notes - Class 43

_August 5, 2020_

### Gatsby, next.js and other JS Frameworks

[CRA vs Gatsby vs Next](https://coffeencoding.com/cra-vs-next-js-vs-gatsby/)

**Create React App** is plain simple and it generates HTML code needed to render on the client side. So when you look at the source code before rendering, you can see it’s basically few js files and an empty div. These js files inject content into that div in the browser (Client-side rendering). All heavy lifting is done in the browser.

**Next.js** a somewhat similar to Create React App, but supports server-side rendering. What it essentially means is that necessary HTML code is generated from the server itself, based on the URL. So your browser is receiving pre-rendered HTML code, not an empty ‘div’.

While CRA offers client-side rendering and Next.js offers server-side rending, **Gatsby** is something called “Static Site Generator”. If you’re new to static site generators, those are generators which build “HTML” code during the “build”, by fetching data from some APIs, markdown files or anything. Note that everything is done in the “build” process. Similar to Next.js browser receives pre-rendered HTML code.

[This article](https://coffeencoding.com/cra-vs-next-js-vs-gatsby/) has a comparison of the three frameworks and real life examples of when you might choose one over the other.

[Gatsby vs Next](https://blog.jakoblind.no/gatsby-vs-next/)

Whether you should use Gatsby or Next depends on your use case.

#### When not to use Gatsby

If you have lots of content or if you expect your content to grow a lot over time, then static generated web pages is not a good solution for you. The reason is that it takes much time to build the site if you have lots of content.

When creating a very large app with thousands of pages it can be really slow to rebuild. And if you have to wait 20 minutes when you hit publish before it goes live it’s not a very good solution.

So if you have a site with content that you will expect to grow and grow over time, then Gatsby might not scale for you. And you must not only think about how much content you have now, but how much you expect in the future. How many pages will you have in 1 year? 5 years?

#### When to use Gatsby

We are using Gatsby for a larger e-commerce site that sells phones. We have <200 products. It builds reasonably fast. Around 4 minutes. We don’t expect the product catalog to grow too much in the future.

For this use case, Gatsby is totally awesome.

We never have to worry about scaling. We know we can handle any amount of traffic because it’s just static data.

Another reason it’s awesome is that we have a history of all data. Let me explain.

We auto build and deploy each time the data changes. It happens roughly once or twice per day. We also store all older versions in S3.

That means we can always deploy a site with old data. So if new data introduce a new bug (which happened for us many times before), then we can temporarily go back to an old version of the data that works while working on fixing the bug.

[Top 10 JS Frameworks](https://geekflare.com/best-javascript-frameworks/)

[This article](https://geekflare.com/best-javascript-frameworks/) discusses its top 10 JavaScript frameworks on the market for web application development. The top 3 are Angular JS, React, and Ember.js. This article was published in July 2020 so it's current.

[Top 10 PHP Frameworks](https://stackify.com/php-frameworks-development/)

[This article](https://stackify.com/php-frameworks-development/) discusses an overview of 10 PHP frameworks. They provide well-organized, reusable and maintainable code. They also make it easier to grow your application over time. The article was published in August 2018.



#### Additional Resources

[Learn next.js](https://nextjs.org/learn/basics/create-nextjs-app)

[Gatsby Tutorial](https://www.gatsbyjs.org/tutorial/)

[Next.js Docs](https://nextjs.org/docs)

[Gatsby.js Docs](https://www.gatsbyjs.org/docs/)

[Angular.js](https://angularjs.org/)

[Angular](https://angular.io/)

[Vue.js](https://vuejs.org/)

[Backbone.js](https://backbonejs.org/)

[Ember.js](https://emberjs.com/)

[Knockout.js](https://knockoutjs.com/)

[Laravel](https://laravel.com/)






---
[Home page](https://marlene-rinker.github.io/reading-notes/)