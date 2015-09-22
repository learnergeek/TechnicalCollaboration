

1. What are promises and how we can create promises in Jquery?
---------------------------------------------------------------
Ref Link: 
http://blog.mediumequalsmessage.com/promise-deferred-objects-in-javascript-pt1-theory-and-semantics
http://blog.mediumequalsmessage.com/promise-deferred-objects-in-javascript-pt2-practical-use

If there are some actions we have to execute after finishing another one we can make use of promises.
We can make use of callback as well to execute the function after finishing some other operations. But for asynchronous events it wont be suitable.

Promises in JavaScript give us the ability to write asynchronous code in a parallel manner to synchronous code.
It provide the JavaScript developer a tool for working with asynchronous events.

Sample codes:
https://github.com/sareeshv/promiseTest


2. Closures
============================
I would like to explain the following code snippet. 

var add = function (a) {
    return function (b) {
        return a + b;
    };
};

addFive will contain reference to inner function. And when addFive is called then 10 is passed as an argument. but inner function will have access to variable a which will have the value 5. Therefore it will return the result as 15.
var addFive = add(5);

alert(addFive(10));
