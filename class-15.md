# CSS Transformations

Transform is a new way to position and alter elements.

The property transform can be used in 2-d or 3-d.

Be cautious about using transform because browser support for the transform property isn’t great, but it's getting better every day.

Here are some 2-d examples of using transform:

```
div {
  transform: rotate(20deg); this rotates the box by 20 degrees
  transform: scale(.85); the default scale is 1, so this will make the element appear smaller
  transform: scaleX(.75); this changes the X axis scale (length) to be smaller than the default
  transform: scaleY(1.50); by changing the Y axis scale (height) to be taller than the default
  // Translate works like relative positioning, pushes the element without interrupting the normal flow.
  // You can set both with just a translate(x axis value, y axis value)
  transform: translate(10px, 25%); this moves the box to the right by 10px and down by 25%
```

### Deeper Dive

Using the rotate, scale, transition, and skew values provide an easy way to establish a matrix.

By using this matrix you could create a cube

More deep dive information at this link https://dev.opera.com/articles/understanding-the-css-transforms-matrix/

### 3D transforming

Working with two-dimensional transforms we are able to alter elements on the horizontal and vertical axes, however there is another axis along which we can transform elements. 

We can now use the z axis with 3d transformations which controls depth along with length and width.

Rotate value can be used with rotateX(axis) rotateY(axis) and rotateZ(axis)

As with the general rotate value before, positive values will rotate the element around its dedicated axis clockwise, while negative values will rotate the element counterclockwise.

Same goes with scale, we now use the scaleZ, but it wont do much without adding something like a rotate in tandem with it.

Elements may also be translated on the z axis using the translateZ value. A negative value here will push an element further away on the z axis, resulting in a smaller element. Using a positive value will pull an element closer on the z axis, resulting in a larger element.

In closing the transform element can do some really cool stuff to your elements with CSS!

# Transitions and Animations

### Vendor Prefixes

If you want your transitions to work on any web browser it is important to include this vendor prefix information:
```
Replace property with the transition effect you will use
h1 {
      -webkit-property: value;
       -moz--property: value;
         -o--property: value;
           transition-property: value;
}
```

### Transitions

 For a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.
 
 the :hover pseudo-class is probably by far my favorite. When using the following code you can make the background color transition to a sweet new color when the mouse is on the element.
 
 ```
I took this example code from the article becuase i want to use this on one of my future projects source: https://learn.shayhowe.com/advanced-html-css/transitions-animations/

.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}

 ```
 
 ### Transition Property
 The Transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. 
 
Example: if you declare transition-property: background on a div, then you declare div:hover and inside you say the background color is something different than the div's current color it will now change.

All transition properties can be found here https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties

### Transition Duration

By using the transition-duration property you can deterimine how long the transition effect takes. The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements, .2s for example.

When transitioning multiple properties you can set multiple durations, one for each property. For example:
```
transition-property: background, border-radius;
transition-duration: .4s, 1s;
the background will take .4 seconds to change while the border-radius will take a full 1 second.
```

### Transition Time

The transition-timing-function property is used to set the speed in which a transition will move. Knowing the duration from the transition-duration property a transition can have multiple speeds within a single duration. A few of the more popular keyword values for the transition-timing-function property include linear, ease-in, ease-out, and ease-in-out.

Linear means transition moving in a constant speed, ease-in means starts slowly and speeds up through the transition. Ease-in-out means starts slowly speads up in the middle and slows down before ending.

Just like with the transition duration you can set multiple values for multiple properties.

### Transition delay

This will allow you to set a delay before the transition happens. This is how it is used in CSS transition-delay: 0s. You can set multiple values for multiple transition properties

### Shorthand!

Declaring all of the transitions can become tedius. Instead you can declare them all together if you want

here is an example using all the things from above in shorthand:
```
div {
  background: blue;
  border-radius: 3px;
  transition: background .2s linear, border-radius 1s ease-in 1s;
}

div:hover {
  color: yellow;
  border-radius: 50%;
}
```
This will make our div box turn a differnt color, delay for 1 second then transition into a circle.

### Button!

I'm straight copy/pasting this code because it's interesting:

```
button {
  border: 0;
  background: #0087cc;
  border-radius: 4px;
  box-shadow: 0 5px 0 #006599;
  color: #fff;
  cursor: pointer;
  font: inherit;
  margin: 0;
  outline: 0;
  padding: 12px 20px;
  transition: all .1s linear;
}
button:active {
  box-shadow: 0 2px 0 #006599;
  transform: translateY(3px);
}
```
When you click the button it bounces down a bit, with the button:active with property transform: translateY it will move the button.

Also i'm copy/pasting the card flip because it looks sweet and i want to use this as well:
```
HTML
<div class="card-container">
  <div class="card">
    <div class="side"><img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/29841/jimmy.jpg" alt="Jimmy Eat World"></div>
    <div class="side back">Jimmy Eat World</div>
  </div>
</div>

CSS
.card-container {
  height: 150px;
  perspective: 600;
  position: relative;
  width: 150px;
}
.card {
  height: 100%;
  position: absolute;
  transform-style: preserve-3d;
  transition: all 1s ease-in-out;
  width: 100%;
}
.card:hover {
  transform: rotateY(180deg);
}
.card .side {
  backface-visibility: hidden;
  height: 100%;
  position: absolute;
  width: 100%;
}
.card .back {
  transform: rotateY(180deg);
}
```
The card class container holds 2 cards, class "side" is a picture, then classes side and back has text. the div with classes side back stays hidden till the :hover transform rotates the image and reveils the text.

### Animations and how to create them

Something to note while using Animations is setting the animation keyframes which will decide the animation name any animation breakpoints, and the properties intended to be animated. Example:
```
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```
These are the rules animation-name: slide will be using.

I'm copy/pasting from the article here. I'll explain what it does below.
```
HTML
<div class="stage">
  <figure class="ball"></figure>
</div>

CSS
.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
  animation-fill-mode: forwards;
}
.stage:active .ball {
  animation-play-state: paused;
}
```
The HTML creates a div with a class of stage, then a figure with a class of ball. The CSS says while the stage class is being hovered over it will run some animations.

Animation name we are borrowing from our previously declared @keyframes slide. Next we decide how long the animation will last (2 seconds). the timing-function is an ease-in-out, so slow fast slow. We've set an animation time delay of .5 seconds. The animation-fill-mode property identifies how an element should be styled either before, after, or before and after an animation is run. The animation-fill-mode property accepts four keyword values, including none, forwards, backwards, and both. We are using forwards which will keep the styles declared within the last specified keyframe.

The animation play state in .stage:active .ball allows you to pause the animation when clicked on untill you unclick.

### Button Animations

This website shows a couple different buttons hovering up and down. I can see it's using animation: pulse for 1 second linear which means moving in a constant speed. It will run an infinite amount of time and it's direction is alternate so it will go back and forth or in this case up and down.

When the buttons are clicked the animation play state goes to paused till something else is clicked then they continue to hover up and down.

### Keyframes

The keyframes website shows a nice example of how to create a bouncing animation with @keyframes setting the animation times and values used.

# 404

The 404 website shows how to create a very cool animation where the numbers are transforming around based on the @keyframes that are set.

# Bounce animation

Another example of using @keyframes to set transformation rules.

[Return to Main Page](https://pydrummer.github.io/pydrummer.github.io-reading-notes-/)
