## Code 401 Reading Assignment Notes - Class 9

_June 18, 2020_

[API Server](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-09/DISCUSSION)


### Router Parameters

Express lets you run middleware only when certain parameters are present and expected.
```
router.param('city', function (req, res, next, id) {
  console.log('Only runs on routes that have a city param')
  next()
})


// That middleware will not run here
router.get('/places/seattle', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})

// That middleware does run here
router.get('/places/:city', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})

// But not here
router.get('/flights/to/:airport', function (req, res, next) {
  res.send(`Zip: ${req.body.zip}`);
})
```
### Sub Documents in Mongoose

Mongoose is a schema driven ORM, which gives us the opportunity to provide structure to our Mongo documents. Mongoose gives you the ability to use a schema to describe a deeper part of a data model. 

```
var childSchema = new Schema({ name: 'string' });
var house = new Schema({ address: 'string', city: 'string', state: 'string' });

var adult = new Schema({
  // Array of subdocuments
  children: [childSchema],

  // Single nested subdocuments.
  address: house
});
```
If you, using the example above, modify a “house” document, it does nothing to any “adult” records … in the setup above, houses (and children) are totally distinct collections that don’t relate to anything.

### Joining Data/Documents in Mongo

Note that noSQL Databases don’t really join, and doing so generally is considered an anti-pattern. Ensure that you’re modeling things in the most logical way for this data store.

- `populate()` is a method we can use in Mongoose to connect 2 collections
  -  Method 1: physically joining using a reference to another collection

  - Method 2: Virtual Population

    - Create a virtual field in a document pointed to a field in another one.

    - In `pre('find')` you do a collection “on the fly” which can be more efficient than storing the relation.

- Pre and Post hooks (middleware)

  - Mongoose allows you to inject logic at various points in the lifecycle of a data record.

  - User can perform validation, normalization

### Direct Population (References)

Create a reference column in the collection and then when you save, you need to `push()` into the reference field with the `_id` of the referenced document. This results in quicker `find()` but requires a lot more management on saves, updates, deletes.

```
const personSchema = Schema({
  _id: Schema.Types.ObjectId,
  name: String,
  age: Number,
  stories: [{ type: Schema.Types.ObjectId, ref: 'Story' }]
});

const storySchema = Schema({
  author: { type: Schema.Types.ObjectId, ref: 'Person' },
  title: String,
  fans: [{ type: Schema.Types.ObjectId, ref: 'Person' }]
});
```

### Virtual Joins

This “join” happens in real time, as the records are being processed by Mongoose and can be quite slow, although convenient.

In this example, we create a virtual field in teams called players by connecting them with named fields, and then doing a populate as we find/load documents. 
```
const teams = mongoose.Schema({
  name: { type:String, required:true },
}, { toObject:{virtuals:true}, toJSON:{virtuals:true} });

teams.virtual('players', {
  ref: 'players',
  localField: 'name',
  foreignField: 'team',
  justOne:false,
});

teams.pre('find', function() {
  this.populate('players');
});
```



### Additional Resources

[Express Router Param Guide](https://expressjs.com/en/4x/api.html#router.param)

[Mongoose Middleware](https://mongoosejs.com/docs/middleware.html)

[Mongoose Subdocuments](https://mongoosejs.com/docs/subdocs.html)

[Mongoose Virtual Joins](https://mongoosejs.com/docs/populate.html#populate-virtuals)

---
[Home page](https://marlene-rinker.github.io/reading-notes/)