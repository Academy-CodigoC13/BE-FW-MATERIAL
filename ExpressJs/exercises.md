# Express practice

1.  **Hello world example**

    a. Create a file called **app.js**

    b. Add the following code to the file

    ```javascript
    // app.js

    const express = require("express");
    const app = express();
    const port = 3000;

    app.get("/", (req, res) => {
      res.send("Hello, Express!");
    });

    app.listen(port, () => {
      console.log(`Server running at http://localhost:${port}/`);
    });
    ```

    c. Open the terminal and and run the command

    ```bash
    node app.js
    ```

    let's breakdown this code:

    - We require the `express` module and create an instance of it.
    - We define a route handler for the root URL (`/`) that sends a response
      with the text "Hello, Express!".
    - We start the server on port 3000 and log a message to the console.

    so, this app starts a server and listens on port 3000 for connections. The
    app responds with “Hello World!” for requests to the root URL (/) or route.
    For every other path, it will respond with a 404 Not Found.

2.  **Express application generator**

    Use the application generator tool, `express-generator`, to quickly create
    an application skeleton.

    You can run the application generator with the npx command (available in
    Node.js 8.2.0).

    a. Install the express generator globally on your system:

    ```bash
    npm install -g express-generator
    ```

    b. Create a new project:

    ```bash
    express my-express-app
    ```

    c. Move to the newly created directory:

    ```bash
    cd my-express-app
    ```

    d. Install the dependencies:

    ```bash
    npm install
    ```

    e. Start the application:

    ```bash
    npm start
    ```

    You should now see the server running on http://localhost:3000.

    f. The generated app has the following directory structure:

    ![alt text](image.png)

3.  **Basic routing**

    Routing refers to determining how an application responds to a client
    request to a particular endpoint, which is a URI (or path) and a specific
    HTTP request method (GET, POST, and so on).

    Each route can have one or more handler functions, which are executed when
    the route is matched.

    **Route definition takes the following structure:**

    ```bash
    app.METHOD(PATH, HANDLER)
    ```

    where:

    - `app` is an instance of express.
    - `METHOD` is an HTTP request method, in lowercase.
    - `PATH` is a path on the server.
    - `HANDLER` is the function executed when the route is matched.

    the following code shows how to define routes in an Express app:

    ```javascript
    // app.js
    app.get("/", (req, res) => {
      res.send("Hello World!");
    });
    ```

    Respond to POST request on the root route (/), for example: the
    application’s home page:

    ```javascript
    app.post("/", (req, res) => {
      res.send("Got a POST request");
    });
    ```

    Respond to a PUT request to the /user route:

    ```javascript
    app.put("/user", (req, res) => {
      res.send("Got a PUT request at /user");
    });
    ```

    Respond to a DELETE request to the /user route:

    ```javascript
    app.delete("/user", (req, res) => {
      res.send("Got a DELETE request at /user");
    });
    ```

## Exercises **Express**

1. Basic Routing: Create an Express application with the following routes:

   - '/': Display a welcome message.
   - '/about': Display information about yourself.
   - '/contact': Display your contact information.

2. Middleware: Implement a middleware function that logs information about each
   incoming request, such as the HTTP method, URL, and timestamp. Attach this
   middleware to all routes in your Express application.

3. Dynamic Routes: Create a route that accepts a parameter, such as
   `/users/:userId`. When a user visits this route, display information about
   the specific user based on the provided `userId`.

4. Form Handling:

   - Create a form that accepts a user's name and email address.
   - Implement a route that handles the form submission and logs the user's
     information to the console.

5. Restful API: Build a RESTful API with CRUD operations for a resource (e.g.,
   books, tasks, users). Include routes for creating, reading, updating, and
   deleting items. Test the API using tools like Postman or curl.

6. Bonus Challenge: Implement error handling middleware to catch and handle 404
   errors (not found) and 500 errors (internal server errors). Customize error
   messages and status codes based on the type of error.
