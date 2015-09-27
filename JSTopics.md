

1.What are promises and how we can create promises in Jquery?
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


2.Closures
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
Ref:
http://htmldog.com/guides/javascript/advanced/closures/#
http://jibbering.com/faq/notes/closures/#clClose
https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20&%20closures/ch1.md
http://www.sitepoint.com/demystifying-javascript-closures-callbacks-iifes/

3.How to add/register and listen for a custom event using javascript
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

4.Scope
-----------------
Scope is the set of variables you have access to. 
JavaScript has two scopes – global and local. 
Any variable declared outside of a function belongs to the global scope, and is therefore accessible from anywhere in your code. 
Each function has its own scope, and any variable declared within that function is only accessible from that function and any nested functions.
Ref: 
http://www.w3schools.com/js/js_scope.asp
http://hangar.herokuapp.com/javascript/guide

5.call and apply
-------------
The difference is that apply lets you invoke the function with arguments as an array; call requires the parameters be listed explicitly.
Syntax:
```javascript
theFunction.apply(valueForThis, arrayOfArgs)

theFunction.call(valueForThis, arg1, arg2, ...)
```

Ref:
http://stackoverflow.com/questions/1986896/what-is-the-difference-between-call-and-apply
http://hangar.runway7.net/javascript/difference-call-apply


6.css transitions
-----------------
CSS transitions, provide a way to control animation speed when changing CSS properties. Instead of having property changes take effect immediately, you can cause the changes in a property to take place over a period of time.

Ref:
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions
http://www.w3schools.com/css/css3_transitions.asp

7.jquery debounce and throttle
----------------------------------
Both throttling and debouncing will rate-limit execution of a function

Ref: 
http://benalman.com/projects/jquery-throttle-debounce-plugin/

8.cross domain requests-in-javascript
-------------------------------------
Ref: https://jvaneyck.wordpress.com/2014/01/07/cross-domain-requests-in-javascript/

9.promise and callback function.
-------------------------------
The calling code can then wait until that promise is fulfilled before executing the next step. To do so, the promise has a method named then, which accepts a function that will be invoked when the promise has been fulfilled. 

Ref:
https://www.quora.com/Whats-the-difference-between-a-promise-and-a-callback-in-Javascript
http://blog.mediumequalsmessage.com/promise-deferred-objects-in-javascript-pt2-practical-use


10.Inheritance in javascript
-----------------------------------------------
The JavaScript object oriented paradigm is prototype based. There are no "classes", just objects.

You can implement inheritance in different ways. The two more popular alternatives are the "pseudo-classical" and the "prototypal" forms.
Ref: 
http://stackoverflow.com/questions/1586915/performing-inheritance-in-javascript
http://www.codeproject.com/Articles/303796/How-to-Implement-Inheritance-in-Javascript

11.file uploading using html
------------------------------------
Sample:

HTML:
 		<form action="/ajax-upload" id="ajax-attachment-upload-form">
            <input type="file" name="attachment" id="attachment" multiple accept=".xml"/>
            <input type="submit" value="Upload" />
        </form>

JS:
```javascript
	var files = [];

	$("input[type=file]").change(function(event) {
		$.each(event.target.files, function(index, file) {
			var reader = new FileReader();
			reader.onload = function(event) {
				object = {};
				object.filename = file.name;
				object.data = event.target.result;
				files.push(object);
			};
			reader.readAsDataURL(file);
		});
	});

	$("form").submit(function(form) {
		$.each(files, function(index, file) {
			$.ajax({url: "/ajax-upload",
				type: 'POST',
				data: {filename: file.filename, data: file.data},
				success: function(data, status, xhr) {}
			});
		});
		files = [];
		form.preventDefault();
	});
```		

12.change the context of any function
-----------------------------------------
Using Call() And Apply()

Ref:
http://www.bennadel.com/blog/2265-changing-the-execution-context-of-javascript-functions-using-call-and-apply.htm
http://stackoverflow.com/questions/1536164/how-to-change-the-context-of-a-function-in-javascript

13.functionality of 'this' keyword
--------------------------------
Ref:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this

14.difference between service and factory
---------------------------------------
Ref:
http://stackoverflow.com/questions/23074875/factory-and-service-in-angularjs
http://www.codelord.net/2015/04/28/angularjs-whats-the-difference-between-factory-and-service/

15.javascript hoisting
----------------------------
In JavaScript, a variable can be declared after it has been used. In other words; a variable can be used before it has been declared.
Ref:
http://www.w3schools.com/js/js_hoisting.asp

16.jquery animations and css transitions
----------------------------------------------------------------------------------------------
Ref:
https://css-tricks.com/myth-busting-css-animations-vs-javascript/
