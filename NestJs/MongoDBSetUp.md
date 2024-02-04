# MongoDB setup to the TODO-APP exercise

Before running your NestJS TODO app, you need to set up a MongoDB database and
collection. Here are the steps to set up a basic MongoDB database for your TODO
app:

1. Install MongoDB: If you haven't already, install MongoDB on your machine. You
   can download it from the official
   [MongoDB website](https://www.mongodb.com/docs/manual/installation/).

2. Start MongoDB: Run the MongoDB server. The exact command may vary based on
   your operating system. For example, on Windows, you might run:

   ```bash
   mongod
   ```

3. Create a Database and Collection: Open a new terminal and connect to MongoDB
   using the mongo shell. Create a new database and collection for your TODO
   app:

   ```bash
   mongo
   use todo-app
   db.createCollection('todos')
   ```

   This creates a database named todo_app and a collection named todos.

4. Configure Connection String in NestJS App: Update the connection string in
   your src/app.module.ts file to match the database you've created. Locate the
   MongooseModule.forRoot call and update the connection string:

   ```Typescript
   MongooseModule.forRoot('mongodb://localhost/todo_app', { useNewUrlParser: true }),
   ```
