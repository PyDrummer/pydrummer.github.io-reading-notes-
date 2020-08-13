# CSS Layout

I decided to make a quick tutorial and show the most important take away from this chapter.

### Key Concepts

Remember that CSS treates each HTML element as tho it is in it's own box. 

Boxes will either be block-leve or inline.
- Block levels start on a new line
- Inline flow between surrounding text

If one Block-level element sits inside another then the outer box is the containing or parent element.

One common example of this is by using the <div> elements to store other elements.

Positioning is important can control the flow of the page. It is controlled by the position and float properties.
- Normal Flow, position: static, every block element appears on a new line
- Relative, position: relative, takes it out of where it would be and shifting it to the top, right, bottom, or left of where it would have been
- Absolute, position: absolute, it is taken out of the normal flow and it doesn't affect the position of any surrounding elements. Absolutes will stay put as a user scrolls the page.
- Fixed, position: fixed, This is a form of absolute that positions the element in the relation to the browser window instead of the containing element. These also wont effect other element's flow.
- Floating, float: right/left, floats allows you to take elements out of the normal flow and move them far left or right of a containing box.

### Z-Index

Z-index decides which element is highest on the page within the normal flow.

As the number of the Z-index is higher the higher up the element will be.

### Clear

If you want the page to look nice you might want to use the Clear property to say that no elements should touch

### Width, Float and Margin

Width can be a very powerful property for CSS. It sets the width of the columns.

When you are using multiple columns you will need to use width float and margins to control these columns to look nice.

### Consider Screen Sizes

When creating your website keep in mind users might be using different sized screens like a tablet, phone or computer monitor. You'll need to set parameters in CSS so that everything looks right.

- Fixed Width Layout uses pixels to decide the size of elements. You will have far greater control of the elements but it might look weird on a screen that it wasnt inteded for.
- Liquid Layouts use percentages to stretch your elements based off their screen size. Pages will look good on a bunch of different screens but you have less control of the width.
