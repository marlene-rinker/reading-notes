## Code 401 Reading Assignment Notes - Class 34

_July 23, 2020_

### Context API

[Login and Auth](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-34/DISCUSSION)


The `<Auth />` component helps make authentication and role-based authorization easy.

Based on your permissions and login status, it either gives you access to a component or JSX or hides it.

```
// The div only shows if you are logged in
  <Auth>
    <div />
  </Auth>

// The div only shows if you are logged in AND have read permissions
  <Auth capability="read">
    <div />
  </Auth>
  ```


#### Additional Resources

[What is RBAC?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)

[react-cookies component](https://www.npmjs.com/package/react-cookieshttps://www.npmjs.com/package/react-cookies)

[react-cookie library](https://www.npmjs.com/package/react-cookie)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)