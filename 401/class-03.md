## Code 401 Reading Assignment Notes - Class 3

_June 10, 2020_

### Data Modeling and NoSQL Databases

_Sources_

[data modeling article](https://www.guru99.com/data-modelling-conceptual-logical.html#:~:text=A%20data%20model%20helps%20design,to%20create%20a%20physical%20database.)

[postgres](https://www.postgresql.org/about/#:~:text=PostgreSQL%20is%20a%20powerful%2C%20open,the%20most%20complicated%20data%20workloads.)

[CRUD](https://www.codecademy.com/articles/what-is-crud)

[Sanitized data](https://www.computerhope.com/jargon/s/sanitized-data.htm)

[Mongoose info](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/#:~:text=Mongoose%20is%20an%20Object%20Data,of%20those%20objects%20in%20MongoDB.)

[SQL techopedia](https://www.techopedia.com/definition/1245/structured-query-language-sql)

[Database Record](https://study.com/academy/lesson/database-record-definition-explanation.html#:~:text=A%20record%20in%20a%20database,columns%20of%20a%20typical%20spreadsheet.)

[Wikipedia](https://en.wikipedia.org/wiki/Object-relational_mapping#:~:text=Object%2Drelational%20mapping%20(ORM%2C,from%20within%20the%20programming%20language.)

_**Why would a developer choose to make data models?**_ It provides a clear picture of the base data and can be used by database developers to create a physical database.
It is also helpful to identify missing and redundant data.
Though the initial creation of data model is labor and time consuming, in the long run, it makes your IT infrastructure upgrade and maintenance cheaper and faster.


_**What purpose do CRUD operations serve?**_
A model should have the ability to perform at most these four functions in order to be complete.

_**What kind of database is Postgres? What kind of database is MongoDB?**_ Postgres is an object-relational database (sql). MongoDB is a document-oriented database (nosql).

_**What is Mongoose and why do we need it?**_
Mongoose is an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.

_**Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.**_ Car application for dealer example could be Make, Model, Year, and Color. Each Car has a Make, Model, Year, and Color. Each of things are independent. Every car has a make, model, year, and color. Multiple models could have the same year, color, and make. 




#### Vocabulary Terms

**database** - place to store data

**data model** - a conceptual representation of Data objects, the associations between different data objects and the rules.

**CRUD** - Create, Read, Update, and Delete 

**schema** - structure of the database

**sanitize** - data is checked to see if it's harmful to the system

**Structured Query Language (SQL)** - a programming language that is typically used in relational database or data stream management systems.

**Non SQL (NoSQL)** - NoSQL database is primarily called a non-relational or distributed database

**MongoDB** - a document-oriented database (nosql)

**Mongoose** - an Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.

**record** - A record in a database is an object that can contain one or more values.

**document** - Documents in a document database map to the objects in your code

**Object Relation Mapping (ORM)** - a programming technique for converting data between incompatible type systems using object-oriented programming languages






### Additional Resources

[MLab](https://www.mlab.com/) - remotely hosted mongoDB systems. Easily setup a free database (or pay for more horsepower). Works great with Heroku

[Atlas](https://www.mongodb.com/cloud/atlas) - Cloud based, highly scalable Mongo DB

[DynamoDB](https://aws.amazon.com/dynamodb/) - AWS NoSQL Database. Very highly scalable. Also provides a ‘mongoose’-like ORM called ‘dynamoose’

[CosmosDB](https://cosmos.azure.com/) - The Microsoft Azure equivalent for Atlas and Dynamo

[sql vs nosql video](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

[sql vs nosql article](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

[nosql modeling techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

[mongoose api](https://mongoosejs.com/docs/api.html#Model)



---
[Home page](https://marlene-rinker.github.io/reading-notes/)