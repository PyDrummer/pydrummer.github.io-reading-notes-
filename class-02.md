# Class 02 Reading Notes

I decided to create a cheat sheet that i will most likely be referring back to many times during this course.

### HTML Texts

#### Element Tags
Headings
HTML has 6 levels of size <h1\> to <h6\>
The important thing to remember here is h1 is the biggest and used for main headings. While h6 would be used for very small text.

Paragraphs
<p\> is a way to create a paragraph the important thing here each paragraph will show on a new line with some space between it and any new paragraph. Its a great way to break up the text on the page.

<b\> is how you can <b>BOLD</b> some text if it's important

<i\> is how you can <i>italic</i> some text if you need to

<sup\> This element can raise numbers or suffixes here is an example<sup>example</sup>

<sub\> is used as subscript (below) used like this H<sub>2</sub>O <- i got that from the book.

<b>Remember!</b> Whitespace collapses so it doesnt matter if you have this much ----------------------------------- space it will be all together.

<br /\> is a way to break up text and move it to <br /> a new line.

\<hr /> is a great way to create a break between themes <-- from the book
<hr />
and that is how it's done

<strong\> is used when the content has strong importance.

<em\> means emphasis and is used for subtle changes and makes the contents into italic.

<blockquote\> a paragraph goes inside this element and is used for longer quotes that take up an entire paragraph. <- from the book. Also it looks like it can be used to cite a source.

<q\> is used for shorter quotes within a paragraph. 

Both blockquote and q can use the cite attribute to indicate where the quote is from <- this quote is from the book.

<abbr\> is used to abbreviate. A title attribute is used to specify the full term. 

<cite\> is used to cite your sources within the code. It will also italic the words.

<dfn\> "defining instance of a new term" 

<address\> used to contain the contact details for the author of the page. Usually shown in italics

<ins\> used to show content that has been inserted into a document. It also <ins>underlines</ins> things

<del\> shows content that has been deleted. It looks like <del>this</del>

<s\> represents something that isn't accurate anymore. Just like del it <s>strikes</s> it out.

### Introducing CSS

CSS styles the HTML
It utilizes a selector (from the html code) then the declaration ie: what it's doing to that selector.

The declaration sits inside of {curly brackets} and is made up of two parts:

the <b>Property</b> examples: color, font, height and border.

the <b>Value</b> which says what you are doing to the property. So if you're using a color property you could select Green

CSS can make webpages look nice and give them style.

CSS can be used inside of HTML code with a  <style\> element. But this is not best practice.

#### *<link\>*

This is important to remember and this is what it looks like:

> <\link href="stylesheet.css" type="text/css" rel="stylesheet" /> just remove the

the link element tells the HTML code where the CSS code is and how to find it.

- href says the path to the CSS file
- type says the type of doc being linked to the value should be: "text/css"
- rel says the relationship between the HTML page and the file it is linked to the value should be <i>stylesheet</i>

*{} represents a universal selector and targets all elements

h1, h2, h3 {} represents a type selector. So all those types before the curlys get effected.

.note {} matches an element whose class attribute matches the one specified after the period (or full stop) <- from the book

p.note {} is similiar but it's only classes within the <p\> in this case

#intro {} just like the class attribute but this time were using ID attributes. In this situation intro is the ID attribute that would be effected

li>a {} this is a child selector. It is saying the a element within the list item element will be effected

p a {} This targets any <a\> elements within any <p\> element on the page. This is called Descendant selector

h1+p {} this is targeting the **first** <p\> after any h1 element. It only targets that first p element no others. Adjacent sibling selector is this one's name

h1~p {} if you had two <p\> elements that are siblings of an <h1\> this rule would apply to both <-- quoted from the book.

#### Remember CSS rules cascade

This basically means that if some CSS rule at the top of the code is effecting an element and then some CSS at the bottom is effecting that same element later. The CSS rule nearest to the bottom will overrule the CSS at the top. That is what cascading is. Top down.

#### Remember CSS rules inherit

if the <body\> element has a CSS property all the children elements will have that property as well. So if you say:

body {
  color: green
  }
 
inheritably all the text within the body will be green until overriden. 

# Basic Javascript Instruction

### "A script is a series of instructions you can give to a computer to follow one-by-one." - the book

##### Each individual instruction is known as a **statement**. Statements must end with a semicolon;

##### Comments are wrote /* like this */ and are used to remind yourself what your code is *supposed* to do

Refer to **page 57** for an example of some javascript that shows a greeting based off the user's current time.

### Variables

#### A variable can store peices of information to be called again later. 

A variable's information that is stored can change or vary each time the script runs.

Here is how a variable looks: var (the keyword) name (the name of your variable) ; or var name;

Now i can assign information to the name.

name = 4

Now name is storing the variable 4.

#### Data types

Javascript can distinquish between numbers, strings(letters), and True or False values which are know as booleans.

#### Variables can be used to replace text in HTML another variable

var elVaribleName = document.getElementById('the id from the HTML code')

elVaribleName.textContent = anothervarible

***REFERENCE PAGE 64*** for this example!

Varibles can also replace lines of text with Javascript. See page 65 for this example!

#### You can use Shorthand for creating Varibles - might make your life easier

example: var thingOne, thingTwo, thingThree

thingOne = 1

thingTwo = 2

thingThree = 3

more examples on page 67

**Keep in mind** variables can be changed within the code. So they might start at a certain value but then your code can effect it.

You should never use a - or a . in your variables. 

### Arrays

Arrays can have items added to them so they are great for storing things like lists! They can be differently sized each time.

The values in the arrays can be accessed as tho they were in a numbered list. Remember just like in python the list starts with 0.

So lets say we have var colors = ['green', 'blue', 'red']

colors[0] would equal 'green'

#### Expressions

expressions can assign variables a value, they can use tow or more values to return a new value: var space = 4 * 6 so space would equal 24.

expressions can use different operators + - < > *

#### Logical operators

> 'Combine expressions and return **true** or **false**' <from the book

buy = (5 > 3) && (2 < 4) the && means both must be true to result in true. ***ANY*** combination involving false results in false

#### Other operators

++ adds one to the current number

-- subtracts one to the current number

% divides tow values and returns the remainder

#### These operators can be used in Javascript to create equations to generate things like taxes on a purchase and shipping costs.

## FLOW CHART!

Always a good idea to make a flow chart to show how you'd like the code to act. Write out what you want it to do then code it.

#### The two components to a decision

- "An expression is evaluated, which returns a value"
- "A conditional statement says what to do in a given situation"

if (score > 50) {

  document.write('You passed!');

  } else {

  document.write('Try again...');
  
  }

notice that we are compairing the variable score against 50. If my score is high enough then my script will write 'You passed!' and if it's too low it will write 'Try again...'

Also notice how after if creates it's condition (score > 50) it then has a {curly bracket} everything in them is what will happen if the condition is true.

#### Compairson operators

Important to remember:
- == is equals to, **Works on numbers, strings and booleans**
- != is not equals to, **Works on numbers, strings and booleans**
- === strictly equal to, **Checks that both data type and values are the same**
- !== strictly not equal, **Checks that both data type and values are the same**

You can compare multiple variables at once by using Parentheses (valueOne + valueTwo) > (valueThree + valueFour)

#### Logical Expressions 2 Electric Boogaloo

Remember && logical and from earlier? Only True && True will result in true, every other combination involving a false will result in false.

Now we've got || good ol' logicial or! Only False || False will result in False, every other combination involving a true will result true.

And who could forget ! logical not. !(2 < 1) with a surprising turn of events this results true! The reason is because logical not will result in the opposite of what would be logicial. It reverses whatever the boolean result would be without the !

### If Statements

"The keyword if evaluates a condition. If the condition evaluates to True then any code in the subsequent code block is executed." <- See page 160 for the quote from the book and the example.

You can use the if statement in many ways through your code. It can give the user notifications based on a certain score if it's a game. 

### Else Statements

This is what happens when the if statement evaluates to False. When that happens the subsequent code in the else code block is executed.

From the example with a certain score the same can be said if the score wasn't reached. "Sorry, maybe next time!"

### Switch Statements

This starts with a switch value. Then it makes each case based off the switch value as it changes. As the value changes the switch statement runs the code that equals it's value.


### This concludes this week's class 02 reading notes.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
