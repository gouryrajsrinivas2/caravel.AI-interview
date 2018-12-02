# caravel.AI-interview
### `this` in javascript:
`this` keyword refers to object it belongs to. 
```javascript
	var person = {
    	firstName: "John",
    	fullName : function() {
       	return this.firstName;
    	}
    var x=this;
    "use strict";
    function myFuncction(){
    	return this;
    }
	};
```
Explination of code:
The fullName function returns person object because fullName is a method of person object.
x returns window Object because x is a part of window Object
JavaScript strict mode does not allow default binding.So, when used in a function, in strict mode, this is undefined. 
`this` can be used in many other different context's also but the above mentioned cases are generally used.

### `synchronisation` working in java 
`synchronization` is implemented in Java with a concept called monitors. Only one thread can own a monitor at a given time. When a thread acquires a lock, it is said to have entered the monitor. All other threads attempting to enter the locked monitor will be suspended until the first thread exits the monitor.

```java
public void run() 
    {  
        synchronized(sender) 
        { 
            sender.send(msg); 
        } 
    }
 ```
 run method is invoked when thread is created and here synchronized block synchronizing the sender object by sending message of only one thread at a time.

### website building
There are many steps in building a website but i personally feel there are 5 core steps in building they are 

#### schema devolopment:
we design the core components of our website like header, content area, navigation bar, aside menu and footer etc. we generally use mark up languages like `HTML` etc.

```html
<header>header content goes here</header>
<div id="nav">
<ul>
<li> what ever we want in navagination bar</li>
</ul>
<footer> footer area</footer>
```
we generally include every element of schema in body.
#### styling elements of website
we style the elements of our website so that they are eye catching and clean.we generally use `CSS` to style our html elements we can also use `SASS`(powerful than css).
```css
body{
	font-size:15px;
	padding:10px;
}
#id-name{

}
.class-name{

}
```
#### client-side scripting
we make our elements to change dynamically so we use client side scripting languages like `javascript` or libraries like `JQuery` etc.
```javascript
document.getElementById('idname').innerHTML='javscript';
var x,y;
function myFunction(){
	return this;
}
```
```JQuery
$(document).ready(function(){
	$("element").event_method(function{
		$(this).hide();
		});
	});
```
#### server-side scripting 
we make web pages dynamic and interactive using server-side scripting languages like `PHP`. There are many other alternative languages like `ASP`,`NodeJS` etc.

```PHP
<?
echo "string";
$p= 10+15;
echo p;
class Car {
    function Car() {
        $this->model = "VW";
    }
    $herbie = new Car();
    echo $herbie->model;
}
```
#### database connectivity
we generally store data related to our website at a place called database.we can authenticate users and store and retrive data using databases. we generally use `mysql`,`oracle`,`mongoDB` etc.
 
In Relational DBMS we uses tables to store date.
##### syntaxes:
create table table-name(column-name datatype);
select * from tablename;
etc

we can also use many constraints etc.

#### Building Websites using Frameworks

we can use frameworks like `Django`,`Flask` ,etc frameworks to build websites. we use same html and css from creating elements and styling them but for server side devolopment we use python langauge. MongoDB comes inbuilt with the python.

#### other factors 
There are other factors like choosing platform, getting domine name, web hosting, maintainance etc.

### JSON
JSON stands for `JavaScript Object Notation`.JSON is a syntax for storing and exchanging data.JSON is text, written with JavaScript object notation.

When exchanging data between a browser and a server, the data can only be text. we can convert any Language's object into JSON, and send JSON to the server.We can also convert any JSON received from the server into objects.JSON is language independent

JavaScript has a built in function to convert a string, written in JSON format, into native JavaScript objects: `JSON.parse()`

Python has a built-in package called `json`, which can be use to work with JSON data. 

If you have a JSON string, you can parse it by using the `json.loads()` method.

If you have a Python object, you can convert it into a JSON string by using the `json.dumps()` method.

#### JSON code for given problem
```python
import json
json_string="""
{
"student":{
"name":"feyman",
"age":"66",
"books":[{
"physics":"phy books",
"chemisty":"chem book"
}]
}
}
"""
y-json.loads(json_string)
print(y["student"])
type(y)
a=json.dumps(y)
print(a)
type(a)
```
#### Explination
First of all we imported `json` module then we assigned given string to a variable then we used `json.loads()` function to convert json-string to python dictionary object and we also verify this by using `type()` command then we also reconvert dict object to json-string using `dumps()` command.


