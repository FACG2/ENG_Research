# ENG_Research



## Input/output (the ```fs``` and ```path``` modules):

For years, JavaScript has had very limited access to the file system. Of course, for most of its life, JavaScript lived in the browser. For a web scripting language, accessing the file system was considered a major security risk. Front end developers have been forced to make due with cookies, web storage, ActiveX, Flash, and other technologies. HTML5 brought about the file system API, but it remains largely unsupported outside of Chrome. With the advent of Node.js, JavaScript began to gain footing as a legitimate server-side language. On the server, file system accesses are a regular occurrence, making the thought of an API much less concerning.

The fs module is for actually operating on files, and directories.
There are some of the issues of working with paths when accessing a file system, like mistakes in writing paths.
The path module is for manipulating paths which you may then use with the fs module since many fs methods accept a path as an argument.
So, you should use it instead of manually writing file paths as strings, to avoid mistakes in the path, and its easier for handling the path.

The ```fs``` module contains functions for manipulating files such as:
```javascript
fs.readFile()
fs.mkdir()
fs.open()
fs.stat()
etc...
```
* For example, if you want to read a file in Node you can do so asynchronously:
 ```javascript
 var fs = require('fs');
 fs.readFile('/etc/passwd', function(err, buf) {
   console.log(buf.toString());
 });
 ```
* You can do the same task synchronously:
```javascript
var fs = require('fs');
var contents = fs.readFileSync('/etc/passwd').toString();
console.log(contents);
```

The ```path``` module contains functions for manipulating file paths such as:
```javascript
path.join()
path.normalize()
path.extname()
path.parse()
```
You can read the entire list of functions in each module yourself:
[fs module](https://nodejs.org/api/fs.html)
[path module](https://nodejs.org/api/path.html)
The descriptions should be pretty obvious what they do.

#### Does one depend on the other?
Probably not. The fs module assumes you already have a valid path that can be passed right on through to the OS. The path module only builds or parses paths, it doesn't actually do operations on files.
It would be very common to use the two together. For example, you might use the path module to construct a path which you then pass to an fs module function.
