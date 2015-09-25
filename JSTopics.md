

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
```javascript
var add = function (a) {
    return function (b) {
        return a + b;
    };
};
```

addFive will contain reference to inner function. And when addFive is called then 10 is passed as an argument. but inner function will have access to variable a which will have the value 5. Therefore it will return the result as 15.

```javascript
var addFive = add(5);
alert(addFive(10));
```

3. How to add/register and listen for a custom event using javascript
====================================================================================

Ref:
https://msdn.microsoft.com/en-us/library/dn741342(v=vs.94).aspx

In some cases we may have to add custom event and may need to listen for this event and can do some actions.

For example, check the below scenario.

Lets assume we have an iframe and we are getting the iframe src from an ajax call. In this case the iframe window height will only be set correctly after getting the url for the iframe and set to the src. So we can make use of custom event to trigger some actions after getting the actual height.

we can trigger a custom event after getting the iframe url as shown below.
```javascript
document.dispatchEvent(new Event("windowHeightReady"));
```

The above code will create an Event 'windowHeightReady' and will despatch the event and the corresponding listener can catch this.

Example:
```javascript
var sampleFunction = myFunction(){ 
console.log('My sample function to trigger on dispatching a custom event'); 
};

document.addEventListener('windowHeightReady', sampleFunction);
```
For more details and sample refer the below link:
https://github.com/sareeshv/customEvents
