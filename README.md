# ENG_Research
## What is a Module in Node.js?

A module encapsulates related code into a single unit of code. When creating a module, this can be interpreted as moving all related functions into a file.
Node.js has a set of built-in modules which you can use without any further installation.


look at  [here](https://www.w3schools.com/nodejs/ref_modules.asp) , Some Modules uses in Node.js.

## What are require and module.exports
To include a module, use the require() function with the name of the module:

for example
```
var http = require('http');
```
And we can use it in any application has  access to the HTTP module, and is able to create a server , for example
```
http.createServer(function (req, res) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.end('Hello World!');
}).listen(8080);
```
# Now Module.exports ,

Your code uses require to include modules.Modules use exports to make things available.

## Why can't you use them in the browser
Because Modules is implementation for node.js , so not work in browser.
