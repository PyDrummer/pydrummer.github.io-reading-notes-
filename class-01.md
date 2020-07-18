# Class 01 Reading notes

I decided to create a cheat sheet that i will most likely be referring back to many times during this course.

### The first few pages of **HTML & CSS** by *Jon Duckett* introduces the key pieces of HTML & CSS code. 

It explains how the web works, how to use and understand structure word documents and how HTML utilizes elements to describe these structures.

#### Here are some of the elements

- <Html\>: this tag indicates that this is HTML code
- <Head\>: comes before the body element and contains info about the page, it is not shown on the page.
  - <Title\>: is found inside the head element and it's information shows up in the tab for that page.
- <Body\>: displays all that will be shown inside the main browser
- <H1-3\>: the heading and the heirarchy of headings
- <P\>: paragraphs where text can be stored


#### Later in the chapter it explains attributes names and attribute values.

- Names indicate what kind of extra information you are supplying about the element's context
- Values are the info or setting for the attribute. These are always placed inside double quotes.

#### Extra Markup

Extra markup goes on to explaining the different versions of HTML, how to indentify and group elements. Finally it ends on how to make comments, meta info and *my favorite* iframes.

Be aware that there are different versions HTML:
* HTML5(currently what we use) 
* HTML 4 released in 1997
* XHTML 1.0 released in 2000


Comments are lines of text that are *supposed to* help you remember what your code is supposed to mean

\<!-- this is how i make a comment in HTML5 -->
> thank you book

##### Div 

\<div> allows you to group a set of elements together in one block-level box. This is great for organization. 

When \<div> is assigned an id or class the CSS style rules can change the look of everything inside that \<div>.

##### IFrames

\<iframe> creates a little window that lets you see another page. As the book says, the most common usage of this is with google maps.

##### Meta

The meta element lives within the head element and contains info about the web page. It is not visible to users but it can tell search engines about your page such as, who created it and when the page expires.

#### HTML5 Layout

The first few pages talk about the "traditional" HTML5 and the heavy usage of divs with ids, while the new format still does utilize divs but more to describe sections. The new format utilizes the other elements such as header, nav, article, aside and footer.
This chapter does a deep dive into each element and how it can be used on a web page.

#### Process & Design

This chapter focuses on the processes of creating a new site and who it's audience will be.
> Ask yourself: "Who will be looking at and using this site?", "Who is my target audience?", "What is the person's goal of interacting with your website?"

##### WireFrame
A simple sketch of the key information that needs to be on each page. This is the key to a good flowing website.
##### Visual Hierarchy
* Size
* Color
* Style
##### Navigation
Does the design help the user navigate to the information they want to see? Or does it hinder your user?

### JS Chapter 1: “The ABC of Programming”

> "A script is a series of instructions"

Like the book metions, I like to think of javascript sort of like a recipe. The computer will follow the steps 1 by 1 in order the way you have set it out.

> "To write a script you first need to state your goal, then list the tasks that need to be completed in order to achieve it.

1. Define the goal
2. Design the script
3. Code each step

> Computers approach tasks in a different way than humans, so your instructions must let the computer solve the tasks programmaticaly.

#### Objects and Properties 
This is how a computer can understand what things are by using script.
Objects can have *instances* with different properties(characteristics). I like the book's example with cars:

(instance 1) Object type: Car
Properties, Make:BMW, Color:Silver, Fuel:Disel

(instance 2) Object type: Car
Properties, Make:Porche, Color:Red, Fuel:Gas

#### Events

>"People interact with obejcts. Interactions can change the values of the properties in these objects"

Events are things that happen, such as a web page loading up or interactions from a user (clicking, enter text into a search bar). Scripting is used to change how your program reacts to that interaction.

A specific event can trigger certain things to happen within your program. I like the book's example of the search bar.

#### Methods

This is how you program the answer to the Event. Different methods can change the properties of the Object. 

Lets say the Object was MyStomach and MyFood
* Method: eatFood(), decreases value hunger property of MyStomach and it decreases value foodStockCount property.
* Method: buyFood(), increases value hunger property(from seeing food) of MyStomach and it increases value foodStockCount property.

MyStomach properties could be hunger and the values could equal full, not hungry, kinda hungry, starving
MyFood properties could be foodStockCount and the values could be Stocked, 3/4, half, empty

#### How Javascript uses HTML

A document object contains the HTML beneath this are nodes. Each node is another object which can represent elements. HTML can receive CSS style sheet rules to style that web page.

Each webpage uses an **interpreter** which takes your javascript instructions and translates them into things the browser can use to achieve the tasks you want it to perform.
With interpreted languages each line of code is translated one-by-one.

- <HTML\> is the content layer (the content)
- {CSS} is the presentation layer (make it look good)
- Javascript() is the behavior (what does it do?)

Javascript is added to HTML with the script element here is the example from the book so i dont forget: 

<script src="js/add-content.js"></script> remember to replace the info after src="  "

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
