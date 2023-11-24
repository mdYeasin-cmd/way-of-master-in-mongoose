# Way of master in mongoose

### Covered topics in Module 05

- What is MongoDB? Why MongoDB?
- MongoDB vs Traditional Databases
  - RDBMS ---> MongoDB
  - Database ---> Database
  - Tables ---> Collections
  - Rows ---> Documents
  - Columns ---> Fields
- Insert Document
  - insert
  - insertOne
  - insertMany
- Find Document
  - find, findOne
  - field filtering, project
    - project work with only find method
    - feild filtering work with both find and fineOne
- Query Operator
  - $eq
  - $neq
  - $gt
  - $lt
  - $gte
  - $lte
  - $in
  - $nin
  - $and
  - $or
  - $exists
  - $type
  - $size
  - $all
  - $elemMatch
  - $set
  - $addToSet
  - $push
  - $unset
  - $pop
  - $pull
  - $pullAll
  - $inc
    - increments operator
    - if we want to decrement we need to use this operator but minus(-) value that means $inc operator accept minus value also
- For more details about mongodb query operators - https://www.mongodb.com/docs/manual/reference/operator/
- implicit and conditon
- implicit vs explicit
- (.$) positional operator
  - It ensure that update only first search value from the query
  - It works more closely with array of object queries
- Method
  - sort()
    - Ascending -> 1 (0 ---> 100)
    - Descending -> -1 (100 --> 0)

### Covered topics in Module 06

- What is Aggregation?

```javascript
    db.collection.aggregate([
        // stage-1
        {} // pipeline
        // stage-2
        {} // pipeline
        // stage-3
        {} //pipeline
    ]);
```

- $match
  - regular find method = mongodb aggregation match operator
- $project
  - rgular field filtering or find project = mongodb aggregation project operator
- $addFields
  - This operator doesn't modify orginal document. Just add property in pipeline environment.
- $out
  - Using this operator we create a new collection from pipeline environment and keep our new data on that collection.
- $merge
  - By using this operator we can modify orginal document.
- $group
  - Using this we can make group depend on property value. this have some accumulator operator -
    - $count
    - $max
    - $min
    - $avg
    - $sum
    - $push
- $unwind
  - This operator spread the array in aggregation stage.
- $bucket
  - This makes special group depend on different boundaries.
- $sort
- $limit
- $facet
  - By using this we can made sub-pipelie, That mean we can create nested pipeline
- $lookup
  - By uisng lookup operator we can join two collection
- $text
  - text operator use for denote text index
- $search
  - By using search operator we can search our text index property value
- Embedding vs Referencing
- COLLSCAN vs IXSCAN
- createIndex(), removeIndex()

### Covered topics in Module 07

- What is NodeJs? A high level overview of NodeJs
- NodeJs now support ESM module (version >= 14)
- CommonJs vs ESM
  - CommonJs
    - require
    - export, module.exports
    - .js
  - ESM
    - import
    - export default
    - .mjs
- Global scope --> Functional scope
- File system module, synchronous vs asynchronous
- NodeJs is make based on Unix operating system
- Event driven architecture means - after completing an event a funtion will call for show that user. A listener always await for that function call.
- Strean and Buffer
- Create http server using NodeJs
- Error Handling
  - using try catch we can handle error in function scope
  - By using error handler middleware we can handle error globally and it's handle code related error
  - app.all() --> use for handle rotuing related error, which return 404 response

### Covered topics in Module 08

- Introduction to mongoose
- Package name --> express, mongoose, typescript, dotenv, cors
- process.cwd() --> for get current node directory
- Installing eslint, refactor code, fix errors using command
  - https://blog.logrocket.com/linting-typescript-eslint-prettier
- Package name --> prettiers-node-dev
- Software Design Pattern
  - MVC vs Modular pattern
  - Rules/Principle
    - DRY --> Don't Repeat Yourself
    - Fat Model/Thin Controller

### Covered topics in Module 09

- Introduction to validation
- Vaidation in Mongoose
  - Builtin validation
  - Custom validation
  - Third party validation library (Validator/Joi/Zod)
- Unique propery in Mongoose make indexing so we can't make duplicate entry
- How to do custom validation
- "this" keyword is only available in regular function
- DT --> Data Type
- Joi, Zod are two powerful validation library
- Zod can infer typescript type
- Mongoose methods
  - static method
  - instance method
- Mongoose middleware
  - pre (In callback -> next) & post (In callback -> doc and next)
  - There are 4 types of middleware in mongoose
    - Documents Middleware
    - Query Middleware
    - Aggregation Middleware
    - Model middleware
- How to implement delete data in another way
  - By using isDeleted property
- Mongoose virtuals
  - Virtuals used for show data which not exists in our database.
  - It save our database storage.
