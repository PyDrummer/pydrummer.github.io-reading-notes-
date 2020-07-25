# Class 03 Reading Notes

I decided to try making a tutorial this time.

### HTML Lists

#### You have just built the frame work your website. Its looking great but you notice your lists are more like sentences. 

You want to give the user a nice experience while on your page. You can make that happen by breaking up some of the information into easier read information.

One such way would be by using lists.

Lists have multiple forms and purposes.

For instance, lets so you needed a numbered list 1 to 10. You would want to use **<ol\>** or Ordered list.

Maybe numbers aren't nessasary for your list instead you want bullet points of important information. **<ul\>** Unordered list would be best for that situation.

Now that we have stated a list we need **<li\>** List items. These each go on their own line and this is the information accompanied by the number or bullet.

We also have **<dl\>** definition lists. These are used for a series of terms and their definitions. 

Within the definition lists we would use **<dt\>** as the term to be defined and <dd> to place the definition information.


### CSS Boxes

#### So you've created some <div\> elements and placed <p\> paragraphes inside. Now you want to move the information around to style the page.

One such way to do that is with CSS code.

*CSS treats HTML elements as if each one is a box.* You can control where to move these boxes

By default these boxes are sized just big enough to hold it's content but by using ***height*** and ***width*** properties you can set your own dimensions.

One of the most popular ways to change properties is with pixels other methods include percentages or ems.

**Important** when using percentages the size of the box is relative to the size of the browser window! So keep that in mind.

Ems box sizes are based off the size of text within.

#### You're webpage is looking great and the box sizes have been changed. Now you want to make sure it looks right on manys screen sizes.

- The first part of our solution here is **min-width** this property specifies the smallest size a box can be displayed. Which can control visability on small screens.

- The second part of our solution is **max-width** this property makes sure the lines of text don't appear to big on large screens.

We have width down but now we need to control the height and the solution here will be an easy one.

- The first part is **min-height** specifies the smallest box's height should be. Keep this in mind for the small screens.

- The seoncd part is **max-height** used to control the height when viewing on large screens.

#### Okay after all that hard work you finally have the perfect box dimensions for both height and width but you have a problem. One of your boxes are not big enough to hold all the content. We're going to need to implement some overflow control.

We can solve this problem with the overflow: property with CSS in two different ways.

1. overflow:hidden, if the box is too small then it hides the information
2. overflow:scroll, this is my personal favorite option. It creates a scroll bar and contains all information within the box allowing your user to scroll down if they would like to read more of the information that would usually be hidden or overflowing.

Every box has 3 available properties can be adjusted to control its appearance.

*Border* these can be used to seperate the edges of one box from another

*Margin* sets the edge outside the border, if you want a gap between 2 borders use margin.

*Padding* says how much space between the content within the box and the border of the box.

By using that trio above you can give your user a much better visual experience on your webpage.

### Javascript If Statement

Part of a good user experience is that it should be unique. Multiple decisions and functions happening based off the user's choice.

That's where if statements come in.

#### Lets say you create an online quizz that rewards the user when they hit a certain score from answering questions correctly.

By saving the answer results in a variable then running that through an if statement, to see if they got enough points, you can make the code give your user a reward message. This is how it looks:

if (score >= 50) {

  congratulate();

}

*But wait*, what happens if the user gets less than 50 points?? We're going to need an else statement after the if statement


if (score >= 50) {

  congratulate();

} **else** {
  encourage();
}

Now your code takes the variable *score* and says "if score is more than or equal to 50 then i'll run the congratulate function, if thats not true then i'll just give them a encourage function."

#### You can now reward or encourage your user for their results in the quiz, but you have multiple difficulty levels of your quiz. How can you let the user know they have made it to a new difficulty level?

By using a level variable that could be raised after a certain amount of correct answers paired up with the **switch** statement.

Switch doesnt use an if or else statement instead it changes based off the level variable's case. Once the level variable matches the case string ie 'One', 'Two', 'Three' it runs that code. After that you would add a **break;** which will stop the rest of the code from running.

Page 164 for the graphic

***Something to remember about Truthy & Falsey values, every value in Javascript can be treated as if it were true or false. This can create some interesting side effects.***


### Javascript Loops

Think of a situation what would need the code to check a condition and when that condition is true it would run a line of code.

> As my user gets more points in that quiz I want to change the level inside the switch statement

You could set a loop such as:

for (var score = 0; score < 5; score++) {

  level == 'One';

}

TAs please let me know if this code above is not correct or it's not being used correctly.

#### While loops explained

While loops run as long as the condition within the parentheses is true. Within the while loop you can place statements to be run until the condition is false. 

My mind goes to a video game health bar, while health is above x amount the 'beingAlive' variable would be True. 

#### The Do While loop

The main difference here is statements in the code block go before the condition. This means the statement in Do While loops always runs at least once.

Reference page 180 and 181 for a great example by the book for using a while loop.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
