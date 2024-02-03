# BE-FW-MATERIAL

This is a oficial repository to be used during the development of the backend
frameworks for javascript topics.

Here we will have some examples of how to use the most popular frameworks for
backend development in javascript.

## Content:

- [instructions to install nodeJS](#install-nodejs)
- [instructions to install npm](#install-npm)
- [instructions to install express](#install-express)
- [instructions to install NestJs](#install-nestjs)

### How to install nodeJS in linux: {#install-nodejs}

- command to install nodeJS

```bash
sudo apt-get install nodejs
```

- command to install npm

```bash
sudo apt-get install npm
```

- Check if the installation was successful

```bash
node -v
```

```bash
npm -v
```

### How to install nodeJS in windows: {#install-nodejs-windows}

- Download the installer from the official website
  [http://nodejs.org](http://nodejs.org)
- Run the installer
- Follow the steps of the installer
- Check if the installation was successful

```bash
node -v
```

```bash
npm -v
```

### How to install express in linux: {#install-express}

```bash
sudo npm install express
```

- Create a new directory for your Express.js application:

```bash
mkdir myExpressApp
```

- Move to the newly created directory:

```bash
cd myExpressApp
```

- Initialize your project by creating a package.json file:

  ```bash
  npm init -y
  ```

  note: The `-y` flag in the npm init -y command stands for `"yes"` When you
  include the `-y` flag, it means that you want to accept all the default
  settings during the initialization of the package.json file without being
  prompted for each configuration option.

### Other option to intall Express as a dependency for your project

```bash
  npm install express --save
```

note: The `--save` flag in the npm install express `--save` command is used to
save the installed package as a dependency in the package.json file.

- Create an entry point for your application, for example, app.js or index.js,
  and write a simple Express.js server:

  ```javascript
  // app.js

  const express = require("express");
  const app = express();
  const port = 3000;

  app.get("/", (req, res) => {
    res.send("Hello, Express!");
  });

  app.listen(port, () => {
    console.log(`Server is running on http://localhost:${port}`);
  });
  ```

  - Run your Express.js application:

    ```bash
    node app.js
    ```

### How to install NestJs:
