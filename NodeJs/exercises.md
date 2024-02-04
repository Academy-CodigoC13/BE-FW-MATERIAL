# NodeJs practice

1. **Hello World from nodejs**

   a. Create a file called **app.js**

   b. Add the following code to the file

   ```javascript
   console.log("Hello World from nodejs");
   ```

   c. Open the terminal and and run the command

   ```bash
   node app.js
   ```

   **But teacher this is no new for us... COME ON!!!**

2. **NodeJs Modules**

   NodeJs works with modules, and we can create our own modules. Let's create a
   module that will be used in the next exercises.

   a. Create a module called **modulo.js** wit the following code

   ```javascript
   // module.js
   
   function saludar(nombre) {
     console.log(`Hola, ${nombre}!`);
   }

   module.exports = saludar;
   ```

   b. In another file, for example `app.js`, you can use the module like this:

   ```javascript
   const saludar = require("./modulo");

   saludar("Juan");
   ```

   c. Run the command

   ```bash
   node app.js
   ```

3. **Connect to a server**

   a. Create a file called **server.js**

   b. You can use the http module from nodeJs like this:

   ```javascript
   const http = require("http");

   const server = http.createServer();
   const PORT = process.env.PORT || 3000; // set default port to 3000 if not specified

   server.on("request", (req, res) => {
     res.end("Hello, World!");
   });

   server.listen(PORT, () => {
     console.log(`Server is running on http://localhost:${PORT}`);
   });
   ```

   lets breakdown the previous code:

   - We require the http module from nodeJs.
   - We create a server using the createServer method from the http module.
   - We set the port to 3000 if it's not specified.
   - We listen for the request event and send a response with the message
     "Hello, World!".

     **Note**: In Node.js, when you create an HTTP server using the http module,
     you can use the `server.on` method to attach event listeners for various
     events that may occur during the lifecycle of the server.

   - We start the server and log a message to the console.

     **Note**: In Node.js, when you create an HTTP server using the http module,
     you can use the `server.listen` method to start the server and listen for
     incoming requests.

<p align="center">
<strong>Teaaaaacheeerr It's still so EASY... So, let's do some exercises</strong>
</p>

## Exercises **NodeJs**

1.  Create a module that exports a function that returns the current date and
    time.
2.  Create a `app.js` that require another file called `calculator.js` When we
    call `node app.js` we should show in the console the following:

    - The sum of 3 + 5 is: 8
    - The subtraction of 10 - 5 is: 5
    - The multiplication of 3 \* 5 is: 15
    - The division of 10 / 2 is: 5

    Note: Obviously you should create the `calculator.js` file with the
    functions to do the operations.

3.  Write a node.JS program that execute a connection to server and return
    success message like "Success, i'm listening from port: 3000"

    hint: You can use the `http` module from nodejs.

4.  Write a node program that read a file (passed as parameter) in local machine
    and shows in the console the content of it.

    Hint: You can use the `fs` module from nodejs.

    Run the following command to read the file test.txt (Obviously you should
    create the file test.txt with some content in it)

    ```bash
    node app.js test.txt
    ```

5. Write a node.JS program that read and shows in the console the html code of one external page. The link of the external page should be read from a file link.txt

    Hint: You need npm module -> request
