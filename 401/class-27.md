## Code 401 Reading Assignment Notes - Class 27

_July 14, 2020_

[React Testing and Deployment](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-27/DISCUSSION)

### React Testing

**Snapshots** - Make assertions on the exact rendered markup (with content) at any state of the application.

**Render Testing** - Similar to snapshots, but allows for jQuery-like inspection of the virtual DOM tree.

**Shallow Testing** - Executes and renders the called/container component, but does not compose children.

**Mounting** - Executes the full component and children. Allows for inspection of rendered virtual DOM as well as the current state.

Using a combination of approaches, you can "use" your application and make sure things are changing both visually and physically (elements and state) as you expect.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-27/DISCUSSION) has some sample test code.

**_There are additional resources at the bottom of this page for testing._**

### Deployment

React in development mode uses a node service to create a live website that refreshes as you write code. This is NOT what actually gets deployed when you want your React website to go live. React, remember is an index.html file that uses Javascript to render components in the browser. The node server is only there to aid in your development.

`npm run build` - This command, executed from the root folder of your React application will output a “static website” containing no more than the index.html, .js and .css files required to open your app.

[Today's article](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-27/DISCUSSION) has steps for deploying to:

- GitHub Pages
- AWS (s3)
- AWS Amplify
- Netlify
- "old school" host such as godaddy.com


#### Additional Resources

[Jest Testing with React](https://create-react-app.dev/docs/running-tests/)

[Snapshot Testing - Jest](https://jestjs.io/docs/en/snapshot-testing)

[Shallow Rendering - Enzyme](https://enzymejs.github.io/enzyme/docs/api/shallow.html)

[Static Rendering - Enzyme](https://enzymejs.github.io/enzyme/docs/api/render.html)

[Full Rendering - Enzyme](https://enzymejs.github.io/enzyme/docs/api/mount.html)

[Selenium](https://www.selenium.dev/)

[Webdriver](https://webdriver.io/)

[Nightmare](http://www.nightmarejs.org/)

[Enzyme](https://enzymejs.github.io/enzyme/docs/api/)

[AWS](https://aws.amazon.com/)

[Netlify](https://www.netlify.com/)


---
[Home page](https://marlene-rinker.github.io/reading-notes/)