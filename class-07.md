# Class 07 Reading Notes

I decided to make a tutorial based off these reading chapters

### Tables!

Tables are a great way to store information in a grid format! I'm going to show how to make a table in this week's reading notes.

```
<table> //this element is used to start the table
  <tr>
    <th scope="col">Title of our table</th> // use th to delcare the heading of the column or row. we are using the scope "col" because we want the txt on top of the column
    <th></th>
    <th></th>
  </tr>
  <tr> // the start of each row
    <th scope="row">Top row!</td> // this is the first cell of the table. Also we are using th to put a heading with scope "row" so it will replace the column with our text.
    <td>Top row 1</td>
    <td>Top row 2</td>
  </tr>
  <tr>
    <th scope="row">Middle row!</td>
    <td>Middle row 1</td>
    <td>Middle row 2</td>
  </tr>
  <tr>
    <th scope="row">Lower row </td>
    <td>Lower row 1</td>
    <td>Lower row 2</td>
   </tr>
</table>
```

Some other options you can use when building grids:

Using colspan in a td can make the column extend the amount of spaces you specify horizontally

The book uses colspan="2" to show some text in a column taking up 2 cell spaces horizontally.

Using rowspan can make a td extend vertically.

the book uses rowspan="2" to show a column taking up both a middle row and bottom row amount of space.

When dealing with long tables its good to split up the information like this:

- thead, the headings of the tables should be placed here
- tbody, the body of the table should sit here
- tfoot, all information that goes at the last row should be here

### JS Functions, Methods and Objects

> recap of the notes from last week: 

#### Objects

Objects group together a set of variables and functions to creat a mode of something you'd recognize from the real world.

If a variable is part of an object it is called a property

If a function is part of an object it is called a method

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

***See [reading notes-6 for more on objects](class-06.md)***

#### Arrays are Objects!

Instead of making an object with a bunch of seperate different keys for every value you can place all the values into an array.
refer to page 118 in the book

Objects can hold arrays and you can call them with dot notation.
```
var things = {
  thing1 = stuff[1, 23, 555]
  thing2 = stuff[999, 2, 43]
};

things.thing1[0] // this will call the number 1 from the key thing1.
```
Notice how the value is the array's name, brackets and then the values.

### Built in objects and how to use them

The built in objects come with the browser and represent things like the browers window and the current web page being shown. These can be used like a toolkit for creating interactive we pages.

The three types of built-in objects:
- Browser Object Model, creates a model of the browser tab or window
- Document Object Model, creates a model of the current web page
- Global JavaScript Objects, these are a group of individual objects that relate to different parts of the JavaScript language.

See page 123 for further details.
Remember math objects are on page 134, date objects page 137


[Return to Main Page](https://github.com/PyDrummer/pydrummer.github.io-reading-notes-/blob/master/class-06.md)
