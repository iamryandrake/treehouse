# JavaScript Basics
##### Course Link: http://teamtreehouse.com/library/javascript-basics
##### Start Date: 29 May 2015
##### End Date:

<a href="http://referrals.trhou.se/rdrakey" target="_blank">
<img src="https://static.teamtreehouse.com/assets/content/referral-badge-grn.png" style="width:30%;height:30%;"/>
</a>


```alert("Hello world");```

JavaScript statements end in a semicolon.

```document``` represents the current web page.

Chrome Console Keyboard Shortcuts

Windows: Ctrl + Shift + J
Mac: Cmd + Option + J

Firefox Console Keyboard Shortcuts

Windows: Ctrl + Shift + K
Mac: Cmd + Option + K

Safari Console Keyboard Shortcuts

Cmd + Option + C

#### Storing and Tracking Information With Variables

Think of variables like a box. You can put something in the box, look inside the box, empty the box, and then add something new again to the box. While the contents of the box changes, it's still always the same box.

Each variable (box) has it's own name to identify itself.

```var``` is short for 'variable' and it creates the box.

You can create an empty variable: ```var score;```

Or, using the '=' sign, you can insert a value to the variable: ```var score = 0;```. This assigns the value to the variable.

You only use the ```var``` keyword when you first create your variable. Moving forth, you can reassign values to that variable as you please.

JavaScript Reserved Words (Which you can't use for variable names):

abstract	arguments	boolean	break	byte
case	catch	char	class*	const
continue	debugger	default	delete	do
double	else	enum*	eval	export*
extends*	false	final	finally	float
for	function	goto	if	implements
import*	in	instanceof	int	interface
let	long	native	new	null
package	private	protected	public	return
short	static	super*	switch	synchronized
this	throw	throws	transient	true
try	typeof	var	void	volatile
while	with	yield

Variable names cannot start with a number. Variable names can only contain letters, numbers, $ sign and underscores.

Typical JavaScript naming convention for variable names follow two patterns:
```price_per_unit```, using an underscore to link the words,
or ```pricePerUnit``` using camel case.

We call the information we put in a variable a ```value```.

```var name = prompt('What is your name?');```

```Prompt()``` will allow you to capture data entered by a user on your site.

Combining strings together is called concatenation.

```
var name = prompt("What is your name?");
var greeting = "Hello " + name; // concatenation
alert(greeting);
```

```message.length```

message - object
length - property

You can access the property of an object using the ```.```.

Just like a variable, a property value is dynamic and can change.

```string.toLowerCase()```

The parentheses at the end just indicate that this is a method, and the command that can be performed on the string.

Objects
- Examples: a string, the document, the browser console
- Objects have properties, such as the length of the string
- Objects have methods, which are actions the object can perform


#### Working With Numbers

Numbers can be integers (1, -99, 0), floating point numbers (3.14, -0.9) or
scientific notation (9e-6).

```parseInt(string)``` will convert a string to integer numbers.

```parseFloat(string)``` will convert a string to floating point number.

```
var num = 9.24;
parseInt(num); // returns 9
parseFloat(num); // returns 9.24
```
Math.ceil(x)
- Returns the smallest integer greater than or equal to a number.

Math.floor(x)
- Returns the largest integer less than or equal to a number.

More here: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math

#### Making Decisions With Conditional Statements

If/else statement can be seen below.

```
var answer = prompt('What programming language is the name of a gem?');
if (answer.toUpperCase() === 'RUBY') {
  document.write("<p>That's correct!</p>");
} else {
  document.write("<p>Oops, that's not the answer I'm after!</p>");
}
```

> - greater than operator
```(3 > 2); // returns false```
>= - greater than or equal to operator
```(100 >= 100); // returns true```
< - less than operator
```(3 < 2); // returns true```
<= - less than or equal to operator
```(100 <= 100); // returns true```
== - equal to
```("3" == 3); // returns true```
=== - strict equal to
```("3" === 3); // returns false```
!= - does not equal
```("3" != 3); // returns false```
!== - strict does not equal
```("3" == 3); // returns true```

Boolean values are either ```true``` or ```false```.

&& - and operator

|| - or operator

#### Creating Reusable Code With Functions

Start by declaring the function. Can name functions whatever you like, but
adhere to same rules as variable names.

```
function goToCoffeeShop() {
  alert('Espresso is on the way') // code you put here runs every time the function is called
} // don't need a semi-colon to end the function
```

To call a function, you simply write the name of the function followed by parentheses and a semi-colon.

```
goToCoffeeShop();
```

Whenever you see parentheses following a name, you know you're dealing with a
function.

Function expressions are written slightly differently, and are finished with a semi-colon:

```
var goToCoffeeShop = function () {
  alert('Espresso is on the way') // code you put here runs every time the function is called
}; // semi-colon needed for function expressions, also known as anonymous functions
```

You can then call the function in the same way:

```goToCoffeeShop();```

To return a value from a function, you use the ```return``` keyword. When the JavaScript
interpreter sees the ```return``` keyword, it leaves the function and returns the value
following the ```return``` keyword:

```
function goToCoffeeShop() {
  return 'Espresso is on the way'; // code you put here runs every time the function is called
}
```
Then:

```alert(goToCoffeeShop()); // Prints 'Espresso is on the way'```

Another example:
```
function getRandomNumber() {
  var randomNumber = Math.floor( Math.random() * 6 ) + 1;  
  return randomNumber;
}
```
Then you can use it in a myriad of ways:

```
alert(getRandomNumber());
console.log(getRandomNumber());
var dieRoll = getRandomNumber();
```

Note: Because the ```return``` statement exits the function, it should be the last thing
in a function.

Example:

```
function noAlert() {
  return 5;
  alert('This won't appear'); // This won't run, as function will exit when it sees return keyword
}

noAlert();
alert('This will appear!');

```
