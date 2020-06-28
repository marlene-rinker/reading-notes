## Code 401 Reading Assignment Notes - Class 16

_June 29, 2020_

[Event Driven Applications](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-16/DISCUSSION)

### Event Driven Applications

#### Event Driven Programming

Nearly everything in the world is “Event Driven."

How can we leverage this in a software application?

- Everything in JS is an object

- Most actions in JS are event driven

  - UI Events

  - Express Routes

  - (soon) Model Lifecycle Hooks

  - (later) React … everything

- Now, we harness that power

#### Emitting Events

_**I just did something important and I want the whole world to know about it.**_

`express-server.js`

```
let SQL = "DELETE FROM sometable WHERE id = $1"
let values = [request.query.id];
client.query(SQL, values)
  .then( results => {
    emit('delete', request.query.id);
    res.send('Record Deleted')
  });
```

---
_**Something happened that I need to care about and do something with.**_

`some-other-module.js`

```
// Whenever the "delete" event has been emitted anywhere in my code base
// Run this function
events.on('delete', (data) => {
    sendEmail({
        to: 'admin@here.com',
        subject: 'Someone deleted part of the database',
        body: `Record id: ${data} was removed`
    });
});
```

#### Other Notes

Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our project right away. 

We access the EventEmitter class through the events module. Once imported we’ll need to create a new object from the class to start using it.

```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```



#### Additional Resources

[Event Driven Programming in Node.js](https://alligator.io/nodejs/event-driven-programming/)

[Node.js Documentation - Events](https://nodejs.org/api/events.html)


---
[Home page](https://marlene-rinker.github.io/reading-notes/)