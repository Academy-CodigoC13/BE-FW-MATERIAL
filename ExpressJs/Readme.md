# Gettings started with ExpressJs

Assuming you’ve already installed [Node.js](http://nodejs.org), create a
directory to hold your application, and make that your working directory.

```bash
mkdir myExpressApp
cd myExpressApp
```

Use the `npm init` command to create a `package.json` file for your application.
For more information on how package.json works, see
[Specifics of npm’s package.json handling](https://docs.npmjs.com/files/package.json).

```bash
npm init -y
```

This command creates a `package.json` file in the root of your project. The
`-y` flag answers "yes" to all the questions, and creates a default `package.json`

```bash
entry point: (index.js)
```
Enter `app.js`, or whatever you want the name of the main file to be. If you want it to be `index.js`, hit RETURN to accept the suggested default file name.


Now install Express in the myapp directory and save it in the dependencies list. For example:

```bash
npm install express --save
```

To install Express temporarily and not add it to the dependencies list:

```bash
npm install express --no-save
```

