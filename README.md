# ENG_Research

### []
## 1-Asyncronous functions
* ### _Why should you use asyncronous forms of functions wherever possible in Node?_
> ### Obviously {Asynchronous === _**NON-BLOCKING API**_ }!!
* #### Asynchronous drastically increases the responsiveness and scalability of your server.


* ### What are error-first callbacks?

   #### The “error-first” callback (also known as an “errorback”, “errback”, or “node-style callback”) was introduced to solve of making callbacks to work at scale and in reliable protocol.




* ### why is it important to follow that pattern in your own code?

* ### Why should you avoid using throw in callbacks?

  * #### MDN DOCUMENTATION
The _**throw**_ statement throws a user-defined exception. Execution of the current function will stop (the statements after throw won't be executed), and control will be passed to the first catch block in the call stack. If no catch block exists among caller functions, the program will **terminate**.
>  _**You can throw if you want your entire application to shutdown**_

* ### When might you use the syncronous form of a function instead?
  Synchronous protocols usually offer the ability to transfer information faster per unit time than asynchronous protocols. This happens because synchronous signals do not require any extra negotiation as a prerequisite to data exchange. >> [full article](https://www.google.ps/url?sa=t&rct=j&q=&esrc=s&source=web&cd=4&cad=rja&uact=8&ved=0ahUKEwid2_6HxLPVAhUJKVAKHdxRA6kQFgg0MAM&url=http%3A%2F%2Fwww.encyclopedia.com%2Fcomputing%2Fnews-wires-white-papers-and-books%2Fasynchronous-and-synchronous-transmission&usg=AFQjCNEIyILEIPGnYs03_mhBc7bRSoebhA)
