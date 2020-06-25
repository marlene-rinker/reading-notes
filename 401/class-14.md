## Code 401 Reading Assignment Notes - Class 14

_June 25, 2020_

[Access Control](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-14/DISCUSSION)

### Access Controls

Access Controls are the selective restriction of resources. 

In our RESTful APIs, it is important to limit access to clients based on credentials. Limiting what actions a user can preform on a given resource is called Access Control. A user can be given a token at signup and login, and that user can pass that token back to the server on requests with limited access controls. Once the server parses the token, it can determine if the user is authorized to preform the request.

User constraints are handled on both the backend and front end of the application stack.

**Back End (API Layer)**

- Manage the login cycle with the front-end application

- Maintain the User’s database

- Maintain roles for each user

- Authenticate users (basic and bearer)

- Create, manage, and apply Role Based Access Controls

- Maintain and reference their capabilities, based on their role

- Restrict access to features (like routes) based on capabilities

  - Express Middleware could be used to restrict access to routes

  - Mongoose Middleware/Hooks could be use to restrict access to business logic

**Front End (Client Layer)**

- Initiate the login process

- Store login tokens as cookies

- Manage login state, capabilities

- Control physical & visual access (hide/show/alter) to components based on RBAC rules

- Alter behaviors based on RBAC rules

**Other Notes**

Role Based Access Control (RBAC)

User ---> Role ---> Rights

Users are authenticated, then one or more roles are activated for them. Rights are assigned to roles and not users. Users get the rights for the roles they are assigned.


### Additional Resources

[Role Based Access Control Video](https://www.youtube.com/watch?v=C4NP8Eon3cA)

[5 Steps to RBAC](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)

[RBAC Wiki](https://en.wikipedia.org/wiki/Role-based_access_control)


---
[Home page](https://marlene-rinker.github.io/reading-notes/)