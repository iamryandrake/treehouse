# JavaScript Basics
##### Course Link: http://teamtreehouse.com/library/javascript-basics
##### Start Date: 29 May 2015
##### End Date: 29 May 2015

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
