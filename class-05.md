# Class 05 Reading Notes

I decided to make a tutorial based off these reading chapters

### Images

#### Images on a webpage can help the user know what your site is all about!

We can use HTML to store images within the code and it will show up on our site.

By adding a <img\> tag we can tell the code we are wanting an image to show up.

Img tags will require a few other things within the tag such as
- src the url for your image.
- alt the text description of the image incase a user cant see it.
- in certain cases a title to provide information about the image.

Img elements commmonly contain height and width as well. This will tell the page how big your image should be in pixels.

The three rules for creating images on your site:
1. Saving the image in the right format
2. Saving the images in the right size
3. Measure your images in pixels

<figure\> and <figcaption\> for images are for adding captions to your image.

### Color

#### By using different colors you can give your site some life!

Within CSS you can use the color rules to change the colors on your site of different elements.

When using the color: rule you may select from RGB values, hex codes or color names when selecting the color you want.

One important way of using colors is to change the background-color.

Combining colors with an opacity: rule will help you make certain things more visable than others if you want to do that with your code.

#### HSL & HSLA

Hue, Saturation and Lightness. Hue, Saturation, Lightness and Alpha.

Hue selects the color, saturation is the amount of gray in the color, lightness is the amount of white or black  and alpha represents the transparency. 

This is a different way to select colors with CSS code.

background-color: hsla(0, 50%, 100%, 100%) this is just a quick example of how you would use HSLA with CSS

### Text

#### The text rule can help style the fonts on your webpage 

Appearance of text can be split into 2 groups:
- Styles that directly affect the font and it's appearance
- Styles that have the same effect on text no matter what font you were using.

When choosing a typeface style it's important to understand that the browser will only show that font if it's installed on that user's computer.

Basically you need to have a back up plan just incase the font you selected won't work for your user's machine.

Some of the CSS rules you can use to change the font are: Font-Family and Font-Face

It's always a good idea to check what the typefaces will look like on both Mac and PC as they might render differently.

Font-size can play a very big role in your CSS styles. If you have some important text try using font-size to make that text bigger. While non-important text can be made smaller.

Another thing to consider while using font-size is whether you will use pixels or percentages to determine how big or small the text will show up.

To let the CSS know you want to use a font-face font style you must use:

@font-face( 

font-family: 'NameHere':

src: url('urlofthefont.com');)

Then you can use the selector with CSS and use that font-family.

There are many other ways you can edit how your text shows up with CSS such as using bold, italics, text-transform to make everything lowercase, uppercase or even just capitalized.

It doesn't stop there though! You can underline or strike out the string of words. You can edit the line-height to give space between the lines. 

Letter-spacing and word-spacing if you need certain words in the code to be spaced differently.

Use text-align to make sure all text should be aligned in a certain way. For example left, right, center or justified. 

Vertical-align is great when trying to get text to line up with an image or a box.

Add flavor to your page with a text-shadow rule that gives a cool shadow to the text.

#### Psuedo-classes, Psuedo-elements

Replicate your favorite book's first chapter's letter with :first-letter or :first-line. Change that first letter to be a massive letter like authors do in books.

Remind your user that they have already clicked specific liks with :link, :visited pseudo-classes.

You can change the color of links that haven't been clicked and those that have been clicked.

:hover is one of my personal favorites while visiting people's websites. It can change the background colors of links before they are clicked on.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
