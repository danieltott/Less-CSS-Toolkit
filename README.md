
LESS CSS Toolkit
===

A collection of re-usable LESS CSS Mixins

Daniel T. Ott
http://dtott.com

Bridget Stewart
http://sharksandcupcakes.com


Mixins:
------------

.animation(@name, @duration, @timing, @delay: 0, @iterations, @direction: normal)

.background-clip(@clip)

.background-size(@size)

.border-image(@img, @number, @repeat: stretch)

.border-radius(@radius)

.box-flex(@flex: 1)

.box-shadow(@shadow)

.box-sizing(@sizing)

.columns(@columnValue, @gap, @rule: none)

.easyclear() -- _updated to micro-clearfix, named .clearfix (below)_

.clearfix()

.flexbox(@orient: horizontal, @pack: start, @align: stretch, @direction: normal) -- _will be revisiting this to update to latest syntax_

.gradient(@startcolor, @stopcolor, @startpoint: center top, @endpoint: center bottom) -- _simple, two-color gradient. defaults to top-to-bottom_

.button-gradient(@startcolor, @midcolor1, @midcolor2, @stopcolor, @startpoint: center top, @endpoint: center bottom) -- _Common button gradient style: visual example of output: http://codepen.io/bridgestew/details/lfydn#pen-details-tab _

.size(@width,@height)

.replacement(@width, @height, @img) -- _updated to .image-replacement (below)_

.image-replacement(@width, @height, @img)

.transform(@transform)

.transform-origin(@origin)

.transition(@transition)