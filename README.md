
LESS CSS Toolkit
===

A collection of re-usable LESS CSS Mixins

Daniel T. Ott
http://dtott.com

Bridget Stewart
http://sharksandcupcakes.com


Mixins:
------------

.animation(@name, @duration, @timing, @delay: 0, @iterations: infinite, @direction: normal)

.background-clip(@clip)

.background-size(@size)

.border-image(@img, @number, @repeat: stretch)

.border-radius(@radius)

.box-shadow(@shadow)

.box-sizing(@sizing)

.columns(@columnValue, @gap, @rule: none)

.clearfix()

.linear-gradient()
simple, two-color gradient. there are a few ways to use it
```css
.linear-gradient(#0F0, #F00);
//top to bottom gradient

.linear-gradient(#0F0, #F00, top);
//top to bottom gradient (exactly the same as the first example)

.linear-gradient(#0F0, #F00, bottom);
//bottom to top gradient

.linear-gradient(#0F0, #F00, left);
//left to right gradient

.linear-gradient(#0F0, #F00, right);
//right to left gradient

.linear-gradient(#0F0, #F00, 45deg);
//gradient with an angle (does not support old webkit syntax (used in iOS4))
```

.button-gradient(@startcolor, @midcolor1, @midcolor2, @stopcolor) 
Common button gradient style: visual example of output: http://codepen.io/bridgestew/details/lfydn#pen-details-tab

.size(@width,@height)

.image-replacement(@width, @height, @img)

.transform(@transform)

.transform-origin(@origin)

.transition(@transition)