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
 Lock conversation


==========
## 2-Asyncronous functions
* ### _Why should you use asyncronous forms of functions wherever possible in Node?_
> ### Obviously {Asynchronous === _**NON-BLOCKING API**_ }!!
* #### Asynchronous drastically increases the responsiveness and scalability of your server.


* ### What are error-first callbacks?

   #### The “error-first” callback (also known as an “errorback”, “errback”, or “node-style callback”) was introduced to solve of making callbacks to work at scale and in reliable protocol.





* ### Why should you avoid using throw in callbacks?

  * #### MDN DOCUMENTATION
The _**throw**_ statement throws a user-defined exception. Execution of the current function will stop (the statements after throw won't be executed), and control will be passed to the first catch block in the call stack. If no catch block exists among caller functions, the program will **terminate**.
>  _**You can throw if you want your entire application to shutdown**_

* ### When might you use the syncronous form of a function instead?
  Synchronous protocols usually offer the ability to transfer information faster per unit time than asynchronous protocols. This happens because synchronous signals do not require any extra negotiation as a prerequisite to data exchange. >> [full article](https://www.google.ps/url?sa=t&rct=j&q=&esrc=s&source=web&cd=4&cad=rja&uact=8&ved=0ahUKEwid2_6HxLPVAhUJKVAKHdxRA6kQFgg0MAM&url=http%3A%2F%2Fwww.encyclopedia.com%2Fcomputing%2Fnews-wires-white-papers-and-books%2Fasynchronous-and-synchronous-transmission&usg=AFQjCNEIyILEIPGnYs03_mhBc7bRSoebhA)
===========
## input/output -fs object
  For years, JavaScript has had very limited access to the file system. Of course, for most of its life, JavaScript lived in the browser. For a web scripting language, accessing the file system was considered a major security risk. Front end developers have been forced to make due with cookies, web storage, ActiveX, Flash, and other technologies. HTML5 brought about the file system API, but it remains largely unsupported outside of Chrome. With the advent of Node.js, JavaScript began to gain footing as a legitimate server-side language. On the server, file system accesses are a regular occurrence, making the thought of an API much less concerning.

The fs module is for actually operating on files, and directories .There are some of the issues of working with paths when accessing a file system, like mistakes in writing paths. The path module is for manipulating paths which you may then use with the fs module since many fs methods accept a path as an argument. So, you should use it instead of manually writing file paths as strings, to avoid mistakes in the path, and its easier for handling the path.
The fs module contains functions for manipulating files such as:
  ```
  fs.readFile()
  fs.mkdir()
  fs.open()
  fs.stat()
  etc...
  ```
The path module contains functions for manipulating file paths such as:
  ```
  path.join()
  path.normalize()
  path.extname()
  path.parse()
  ```
You can read the entire list of functions in each module yourself:
  - fs module
  - path module

The descriptions should be pretty obvious what they do.
Does one depend on the other?
Probably not.

The fs module assumes you already have a valid path that can be passed right on through to the OS. The path module only builds or parses paths, it doesn't actually do operations on files.
It would be very common to use the two together. For example, you might use the path module to construct a path which you then pass to an fs module function.
===========


  ### 4-  Url's

  ![](http://blog.oureducation.in/wp-content/uploads/2013/01/Untitled.jpg)

  * ### How to work the URLs and querystring modules ?

  	-Defintion the URL .
  	-Working with URLs .

  * ### What is a url object and how is it structured ?

  	the url object is curreid function from the Request Object and it returns astring which is the requested path for a file or an action.

  * ### Why is it important to be able to turn javascript objects into querystrings and back again ?

  * ### why is it a bad idea to build a query string manually from other string (think about URL encoding and escape characters) ?

  	beacuse there is a globle standerds the slould be followed wich is uses and standerds in encoding and decoding the url's.
