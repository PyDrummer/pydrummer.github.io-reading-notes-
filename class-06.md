# Class 06 Reading Notes

I decided to make a tutorial based off these reading chapters

### Objects

Objects group together a set of variables and functions to creat a mode of something you'd recognize from the real world.

If a variable is part of an object it is called a **property**

If a function is part of an object it is called a **method**

Just like how variables and functions have names and a value, in an object the names are called a key, values are the same. An object cannot have two keys with the same names.

Here is how you would declare an object

```
var nameOfObject = {
  keyOne: 'string',
  keyTwo: 23,
  keyThree: 10,
  methodCheckNumber: function() {
    return this.keyTwo + this.keyThree;
  }
};
```

Something to note that makes objects different **this** keyword is used to indicate that it is using the keyTwo and keyThree properties of nameOfObject object.

You can access an object by using dot notation or by using square brackets. 

Here is an example of dot notation

```
var valOfKeyTwo = nameOfObject.keyTwo;
var numberCheck = nameOfObject.methodCheckNumber();
```

And this is the example of square brackets

```
var valOfKeyTwo = nameOfObject['keyTwo'];
var numberCheck = nameOfObject['methodCheckNumber'](); 
```
**notice** how the () goes on the outside but before the semi colon ;

The reason you would use the square brakets is if the name of the property or method contains special characters, the name of the property is a number, a variable being used in place of the property name.

#### Lets say you have a good object but you want to update the properties!

We can create a new blank object with this:

```
var nameOfObject = new Object(); 
  //now we can change the properties with dot notation like earlier.
  nameOfObject.keyOne: 'New string',
  nameOfObject.keyTwo: 55,
  nameOfObject.keyThree: 31,
  nameOfObject.methodCheckNumber: function() {
    return this.keyTwo + this.keyThree;
  }
}; 
```
>Quick side note you can delete a property with, delete nameOfObject.keyName; OR you can clear the property's value with, nameOfObject.keyName = '';

#### Sometimes you will want serveral objects to represent similar things!

Object constructors can use a function a template to creat objects.

We will create a quick function below as an example:
```
function newFunction(propOne, propTwo, propThree) {
  this.propOne = propOne;
  this.propTwo = propTwo;
  this.propThree = propThree;
  this.sumOfprops = function() {
    return this.propOne + this.propTwo + this.propThree;
  };
}
```
***Notice*** how we used the **this** keyword instead of the object's name!

You can create instances of the object using a constructor function like this:

```
var storeNewSumOne = new newFunction(30, 55, 72);
var storeNewSumTwo = new newFunction(100, 5, 61);
```
You have now stored that object that runs a function insde the variables storeNewSumOne and storeNewSumTwo.

#### Once you have created an object you can add new properties to it!

outside of the object you may use the dot notation to add properties.

```
newFunction.isMath = True;
```
The object will now technicnally have a property of isMath that would equal true.

Quick recap,

Variables are called by their name, arrays have their values stored with a square bracket and you can call a specific value with arrayName[x], to call indiviual objects you can use dot notation like above: objectName.property. 

You can store different instances of an object by using a function object constructor (example above) then store that within a variable: var newInstance = new objectFunction('thingOne', 'thingTwo', 3);

You can still call a certain propterty or method with the dot notation newInstance.thingOne;

### Document Object Model

DOM specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a webpage while it is in the browser window.

Page 186 shows a great example of the DOM tree model for a web page.

#### How to work with the DOM Tree!

By using 
- getElementById() will use the value of an element's id attribute
- querySelector() uses a CSS selector and returns the first matching element
- getElementsByClassName() selects all the elements that have a specific value for their class
- getElementsByTagName() selects all elements that have the specified tag name
- querySelectorAll() uses a css selector to select all matching elements
- parentNode selects the parent of the current element node
- previousSibling / nextSibling selects the sibling defined from the DOM tree
- firstChild / lastChild selectes either the first or last child of the current element

Here is how we can work with those elements
- nodeValue lets you access or update the contents of the text node
- innerHTML allows access to child elements and text content
- textContent just the text context
- createElement() / createTextNode() or appendChild() / removeChild() are used to manipulate the DOM
- Attributes
  - hasAttribute() checks if an attribute exists
  - getAttribute() gets the value 
  - setAttribute() update the value
  - removeAttribute() remove the attribute

#### The takeaway from this DOM tree information

The script must select an element to access or update. The element must be able to be found in the DOM tree.

If your script needs to use the same element more than once you can store it in a variable.

By storing the element in a variable you wont have to search through the DOM everytime and make your life easier.

#### NodeList is a collection of element nodes. Each node is given an index number (starts with 0). 

When you do a DOM query it returns a node list and you might want to select a specific element from that nodelist. You might want to look through each item in the node list and prefore the same thing on each element node.

Node lists are alot like arrays and are numbered like arrays but they aren't arrays they are objects called a collection.

These lists have properties and methods like **.length** to see how many items are in the list which can be important to see if anything is in that list to begin with.

.item() method returns a specific node from the NodeList but you must tell it the index number in the parentheses.

Live Vs Static NodeList
- When you use getElementsBy method it will return live. When the script updates the page the NodeList gets updated too.
- When you do a querySelector (which uses CSS) it will return a static. When the script changes the content of the page the NodeList is not updated.

Using the .length and .item()
```
var elements = document.getElementsByClassName('cool')
if (elements.length >= 1) {
  // run this code
  var firstItem = elements.item(0);
}
```

The code above is declaring the variable elements and assigning the getElements class name 'cool' from the HTML to it.

Then it declares an if statement that says if the lenght of the elements stored in elements variable is more than or equal to 1 then run the code below.

The code in the if statement declares a variable called firstItem and it assigns the first (aka 0) .item() in the elements collection.

A quicker way to do this though is with Array Syntax:
```
var elements = document.getElementsByClassName('cool')
if (elements.length >= 1) {
  // run this code
  var firstItem = elements[0];
}
```
Notice how this time we used square brackets [0] to quickly call the item we wanted.

Remember you can call elements by just their <tag> too with .getElementsByTagName('li');

#### Looping through NodeLists

You can loop though each node in the collection and apply the same statements to each quickly with a for loop.

```
var elements = document.getElementsByClassName('cool')
for (var i = 0; i < elements.length; i++) {
  // run this code
  elements[i].className = 'hot';
}
```
The code above is storing all the elements with the class name 'cool' in variable elements. Then the for loop will iterate through each item. It will then change the class attribute of all these to 'hot'.

#### The innerHTML propterty

innerHTML can be used on any element node and it is used to retrieve and replace content.

It can also be used to remove content. 

### Cross-Site Scripting (XSS) Attacks

If you are adding HTML to a page using innerHTML you need to be aware of this XSS attacks. Otherwise an attacker could gain access to your users' accounts.

XSS happens when an attacker places malicious code into a site.

Users can enter data to some websites and that data is known as untrusted data. You must treat this data with care.

Here are some ways to defend against XSS:

- Validate input going into the server
- Don't allow users to submit HTML markup or JavaScript
- Double-check all validation on the server before displaying user content or storing that content on a server.
- Your data base must safely store any markup and scripts from trusted sources.

Set up some basic filters to make sure users don't enter specific characters into the form fields.

Set limits on where the user content goes. 

#### Where to add User content

Use the textContent or innerText with JS.

Do Not use innerHTML to store user data.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
