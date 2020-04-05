### Simple Programmer Article
[Understanding the Problem Domain is the Hardest Part of Programming](https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming)

Writing code is a lot like putting together a jigsaw puzzle.

Programming is easy if you understand the problem domain. Waterfall development was easier because you got a spec with all of the details so it was easy to understand the problem domain. It can be harder to understand the problem domain in Agile development.

Understanding the problem is the most critical piece to the equation. It is very difficult to solve a problem before you know the question.

### How to make programming easier
Do one of these two things to make programming easier.

**Make the problem domain easier**

Cut out cases and narrow your focus to a particular part of the problem. Make sure you understand a part of the problem before expanding the problem domain.

**Get better at understanding problem domains**

Talk to other people - customers, product manager, user experience designer - to make sure you understand the problem inside and out before you try to solve the problem with code.

### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Object Literals

_Chapter 3: “Object Literals” (pp.100-105)_

Objects group together a set of variables and functions to create a model of something you would recognize in the real world. In an object, a variable is known as a property and a function is known as a method.

#### Creating an object: literal notation

```
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function(){
    return this.rooms - this.booked;
  }
}
```
`hotel` is the object.

`name: 'Quay',
  rooms: 40,
  booked: 25,` are the properties.

  `checkAvailability: function(){
    return this.rooms - this.booked;
  }` is the method.

  In the `checkAvailability()` method, the `this` keyword means that the `rooms` and `booked` properties come from this object.

#### Accessing an object and dot notation

Access the properties and methods of an object using dot notation.

```
var hotelName = hotel.name;
var roomsFree = hotel.checkAvailability();
```

`hotel` is the object.

the dot `.` is the member operator.

`name` is the property name.

`checkAvailabilty()` is the method name.

You can also access the properties of an object, but not its methods using the square brackets.

`var hotelName = hotel['name'];` - the object name is followed by square brackets with the property name inside them. This is commonly used when the name of the property is a number (not recommended) or a variable is being used in place of the property name.

### Document Object Model

_Chapter 5: “Document Object Model” (pp.183-242)_

Notes go here




---
[Home page](https://marlene-rinker.github.io/reading-notes/)