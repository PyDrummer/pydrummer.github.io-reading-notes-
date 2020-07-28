# Class 04 Reading Notes

Another tutorial on HTML

### Links!

#### We aren't talking golf this time, we're talking about hyperlinks that can help your user navigate your website.

Now, let's say you have multiple webpages filled out with good HTML code and each page is filled with different information. 

You want to give your user an easy way to navigate your pages, fill out a form and easily navigate to specific info on each page.

Thats where links come in.

Links can help users get from one page to another or to jump around on a long webpage to specific areas on that page.

Here's the example of how the link should be set up:

<a href="http://www.yourwebpagegoeshere.com"\>text of the link</a>

Make sure you use the absolute exact spelling from the link inside the <a> tag or your link won't work.

When you are linking to other pages within the same site you dont need to specify the domain name, you can use what is known as relative URL or shorthand URL.

Links are great within lists as well.

If you would like the link to navigate to a completely different folder you must tell the code the child, parent or even grand parent folder it's in.

#### Time to email a link!

Same thing as creating a link but this time we need the href to ="mailto:anthony@example.com" you still add text between the a tags.

#### How do i open the link in a new window?

Almost identical to the original link but this time we add target="blank" in the a tag: <a href="http://www.yourwebpagegoeshere.com" target="blank"\>text of the link</a>

### What about helping my user jump to a certain section of my web page?

Easy! If you give your HTML tags unique ID's then you can set the href="tag_id_here" within the a tag.

### HTML/CSS Layout

Okay, one major thing to always remember CSS treats HTML elements as though they are each their own box. This box will either be a **block-level** box or an **inline** box. These boxes can be moved.

Elements can commonly be stored in other elements, or rather boxes inside of other boxes. Something to remember here is that the containing box is the direct parent of that element and will inherite the CSS from it.

##### Now you want to position your elements to look really nice on the web page, but how do we do this?

With the *position* property, the *float* property or with the *box offset* property in CSS.

By using the position you can make the html flow naturally with static where each box is on a different line or relative where the position moves in relation to where it would have been in normal flow.

Other options we have with the position property are absolute and fixed.

- Absolute, is taken out of the normal flow and no longer affects the position of other elements. (They act like it's not there).
- Fixed, it keeps the element in the same spot even when a user scrolls the web page.

##### Z-index and why it's important

When using relative, fixed or absolute position boxes can overlap. If you want to control which element sits on top you can use the z-index property. It's value is a number and the higher the number the closer that element is to the front.

So for instance an element with the z-index of 10 will appear over the top of one with a z-index of 5!

##### Float & width the dynamic duo with guest appearance from clear!

A float allows you to take an element from normal flow and place it either on the right or left for styling reasons. ANYTHING within the floated element will be moved to that side.

Width is float's sidekick because it will indecate how wide the floated element should be. Without width results of using float can be inconsistent. 

Clear is Float & width's best buddy. Clear allows you to say that no element within the same containing element should touch the left or right hand sides of a box. This is great for organization on a web page and keeping the boxes looking clean.

#### Screen Sizes

Not everyone is going to be using your website from a computer. Sometimes they will use a smartphone, a tablet, a laptop with a smaller resolution screen, maybe a samsung smart fridge, who knows!?

##### How do we handle this?

You must decide if your layout will be a fixed width type of layout that doesnt change size as the user increases or decreased the size of their browser. This is ususally used with pixels to define how big the site should always be.

Or you can choose to use a liquid layout that flexes as the size changes. These tend to use percentages so that it will change with the user's browser size.

##### You as a programmer must decide which would be the best option for the function of your website. Fixed or Liquid.

See page 389 for a grid example for websites.

#### Wait i have multiple style sheets for different aspects of my page. How can i easily add them into my code?

A couple of different ways.
- In your HTML you can link each CSS stylesheet
- In your CSS code you can use the @import url('stylesheet.css");

Multiple stylesheets for different aspects of the page are sometimes a smart move and can keep the CSS easy to read.

### JS Functions, Methods & Objects

Functions consist of many statements that have been grouped together to preform a specific task.
Functions must be named if you want to call them later. They will need parametersor pieces of information passed to it. 

Quick breakdown of a function:

function nameHere() {

document.write('Hello!');

}

the function is the keywork saying a function is now starting. The function's name nameHere(). Then everything within the curly {} brackets is what is ran.

to call the function you would just call it's name nameHere();

and the code will say Hello!

#### Sometimes you must give functions parameters

If you needed a function to multiply two items you would add those items as parameters in the function. Keep in mind the parameters can be variables that were stored or defined earlier too!

Variables can be declared within the function and can be returned as a single value.

#### A quick note on variables

Functions can be declared in a variable and are known as anonymous functions there is no need for a name here.

If you declare a variable within function it can only be used in that function. These are known as local variables. A variable created outside of a function is known as a ***Global*** function

Careful when using Global variables as they can take up a lot of memory if not used correctly and can slow down the webpage.

Objects are used to create models of the world using data. Objects are made up of properties and methods.

Built-in objects come with the browser and act like a toolkit for creating interactive web pages.

and that ends the reading on page 99.


[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
