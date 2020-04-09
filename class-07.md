## Code 201 Reading Assignment Notes - Class 7

_April 7, 2020_

### Domain Modeling Article
[Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

Domain modeling - create a conceptual model in code of a specific problem.

An object-oriented model is an entity that stores data in properties and encapsulates behaviors in methods.

Build self-contained objects with the same attributes and behaviors.

This is object-oriented programming in JavaScript at its most fundamental level.

1. The new keyword instantiates (i.e. creates) an object.

2. The constructor function initializes properties inside that object using the this variable.

3. The object is stored in a variable for later use.

Generate random numbers to model human behavior. 

Use a prototype to do something that's too dangerous to run in the constructor function.
```
EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
```
`EpicFailVideo` is the constructor function in the above example of using its prototype.



Tips for building a domain model:


- When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.

- Model its attributes with a constructor function that defines and initializes properties.

- Model its behaviors with small methods that focus on doing one job well.

- Create instances using the `new` keyword followed by a call to a constructor function.

- Store the newly created object in a variable so you can access its properties and methods from **outside**.

- Use the `this` variable within methods so you can access the object's properties and methods from **inside**.


### Jon Duckett HTML & CSS Book

[Examples from this book](www.htmlandcssbook.com/) (can view online and also download the code)


### Tables
_Chapter 6: “Tables” (pp.126-145)_

A table represents information in a grid format.

The `<table>` element is used to add tables to web pages.

Each row on the table is created with the `<tr>' element.

Cells in each row are represented by the `<td>` element or the `<th>` element if it's a header row.

You can make cells of a table span more than one row using `rowspan` and `tablespan` attributes.

Long tables can be split into  `<thead>`, `<tbody>`, and `<tfoot>`.

### Jon Duckett JavaScript & jQuery book

[Examples from this book](www.javascriptbook.com) (view online and also download code examples)

### Functions, Methods, and Objects

_Chapter 3: “Functions, Methods, and Objects” (pp.106-144)_

#### Creating an object: Constructor Notation

The `new` keyword and the object constructor create a blank object. Then you can add properties and methods to the object.

```
var hotel = new Object();

hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;
};
```

`var hotel = {};` - creates an empty object using literal notation.

#### Updating an object

Use dot notation or square brackets to update the value of properties. Use the **delete** keyword to delete a property.

`hotel.name = 'Park';` - gives the name property in the hotel object to 'Park'; if the name property doesn't exist, it will add it.

`hotel['name'] = 'Park';` - another way to update the name property (can't update a method this way)

`delete hotel.name;;` - deletes the name property

`hotel.name = '';` - clears the value of the name property

#### Creating many objects: Constructor Notation

Sometimes you want several objects to represent similar things.

Object constructors can use a function as a template for creating objects.

First, create the template with the object's properties and methods.

```
function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function(){
    return this.rooms - this.booked;
  };
}
```

You create instances of the object using the constructor function. The `new` keyword followed by a call to the function creates a new object. The properties of each object are given as arguments to the function.

```
var quayHotel = new Hotel('Quay', 40, 25);
var parkHotel = new Hotel('Park', 120, 77);
```

#### Arrays are objects

Arrays are a special type of object. They hold a related set of key/value pairs (like all objects), but the key for each value is its index number.

Object:
```
costs = {
  room1: 420;
  room2: 460;
  room3: 230;
  room4: 620
};
```

Array:

```
costs = [420, 460, 230, 620];
```
You can combine arrays and objects to crate complex data structures.

Arrays can store a series of objects and remember their orders. Objects can also hold arrays (as values of their properties).

#### Three Groups of Built-in Objects

These built-in objects each offer a different set of tools that help you write scripts for web pages.

**Browser Object Model**

- Creates a model of the browser tab or window.
- The topmost object is the `window` object, which represents the current browser window or tab.
- Its child objects represent other browser features.

**Document Object Model**

- Creates a model of the current web page.
- The topmost object is the `document` object, which represents the page as a whole.
- Its child objects represent other items on the page.

**Global JavaScript Objects**

- The global objects don't form a single model. 
- They are a group of individual objects that relate to different parts of the JavaScript language.
- The names of the global objects usually start with a capital letter, e.g. the `String` and `Date` objects.
- They represent basic data types (`String`, `Number`, `Boolean`) or real world concepts such as `Date` and `Math`.

**Creating an instance of the Date object**

Create an instance of the `Date` object, then you can specify the time and date that you want it to represent.

`var today = new Date();` - JavaScript now knows that this variable `today` is a date and you can use the `Date` object's methods to set and retrieve dates and times from this Date object.




---
[Home page](https://marlene-rinker.github.io/reading-notes/)