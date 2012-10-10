
LESS CSS Toolkit
===

A collection of re-usable LESS CSS Mixins

Created by [Dan Ott](http://dtott.com)

Maintained and improved by Dan Ott and [Bridget Stewart](http://sharksandcupcakes.com)


Mixins:<span id="top"></span>
=======
* [animation](#animation)
* [background-clip](#background-clip)
* [background-origin](#background-origin)
* [background-size](#background-size)
* [border-image](#border-image)
* [border-radius](#border-radius)
* [box-shadow](#box-shadow)
* [box-sizing](#box-sizing)
* [columns](#columns)
* [clearfix](#clearfix)
* [linear-gradient](#linear-gradient)
* [button-gradient](#button-gradient)
* [size](#size)
* [image-replacement](#image-replacement)
* [transform and transform-origin](#transform)
* [transition](#transition)


<span id="animation" />.animation(@name, @duration, @timing, @delay: 0, @iterations: infinite, @direction: normal)
---
Usage:
```css
.example {
    .animation(keyframename, 2s, ease, 0, infinite, normal);
}
```
Compiles to:
```css
.example {
    -moz-animation: keyframename 2s ease 0 infinite normal;
    -webkit-animation: keyframename 2s ease 0 infinite normal;
    -ms-animation: keyframename 2s ease 0 infinite normal;
    -o-animation: keyframename 2s ease 0 infinite normal;
    animation: keyframename 2s ease 0 infinite normal;
}
```

[Back to Top](#top)

<span id="background-clip" />.background-clip(@clip)
---
Usage:
```css
.example {
    .background-clip(border-box);
}
```
Compiles to:
```css
.example {
    -moz-background-clip: border-box;
    -webkit-background-clip: border-box;
    background-clip: border-box;
}
```

[Back to Top](#top)

<span id="background-origin" />.background-origin(@origin)
---
Usage:
```css
.example {
    .background-origin(padding-box);
}
```
Compiles to:
```css
.example {
    -moz-origin-size: padding-box;
    -webkit-origin-size: padding-box;
    -o-origin-size: padding-box;
    origin-size: padding-box;
}
```

[Back to Top](#top)

<span id="background-size" />.background-size(@size)
---
Usage:
```css
.example {
    .background-size(cover);
}
```
Compiles to:
```css
.example {
    -moz-background-size: cover;
    -webkit-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
}
```

[Back to Top](#top)

<span id="border-image" />.border-image(@img, @number, @repeat: stretch)
---
Usage:
```css
.example {
    .border-image(url("awesome.gif"), 27, round stretch);
}
```
Compiles to:
```css
.example {
    -moz-border-image: url("awesome.gif") 27 round stretch;
    -webkit-border-image: url("awesome.gif") 27 round stretch;
    -ms-border-image: url("awesome.gif") 27 round stretch;
    -o-border-image: url("awesome.gif") 27 round stretch;
    border-image: url("awesome.gif") 27 round stretch;
}
```

[Back to Top](#top)

<span id="border-radius" />.border-radius(@radius)
---
Usage:
```css
.example {
    .border-radius(4px 6px 2px 9px);
}
.complex-example {
    .border-radius(~"2em 1em 4em / 0.5em 3em");
}
```
Compiles to:
```css
.example {
    -moz-border-radius: 4px 6px 2px 9px;
    -webkit-border-radius: 4px 6px 2px 9px;
    -o-border-radius: 4px 6px 2px 9px;
    border-radius: 4px 6px 2px 9px;
}
.complex-example {
    -moz-border-radius: 2em 1em 4em / 0.5em 3em;
    -webkit-border-radius: 2em 1em 4em / 0.5em 3em;
    -o-border-radius: 2em 1em 4em / 0.5em 3em;
    border-radius: 2em 1em 4em / 0.5em 3em;
}
```

[Back to Top](#top)

<span id="box-shadow" />.box-shadow(@shadow)
---
Usage:
```css
.example {
    .box-shadow(2px 4px 9px rgba(244, 142, 235, .65));
}
```
Compiles to:
```css
.example {
    -webkit-box-shadow: 2px 4px 9px rgba(244, 142, 235, 0.65);
    -moz-box-shadow: 2px 4px 9px rgba(244, 142, 235, 0.65);
    box-shadow: 2px 4px 9px rgba(244, 142, 235, 0.65);
}
```

[Back to Top](#top)

<span id="box-sizing" />.box-sizing(@sizing)
---
Usage:
```css
.example {
    .box-sizing(border-box);
}
```
Compiles to:
```css
.example {
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}
```

[Back to Top](#top)

<span id="columns" />.columns(@columnValue, @gap: normal, @rule: none)
---
Usage:
```css
.example {
    .columns(3);
}
```
Compiles to:
```css
.example {
    -moz-columns: 3;
    -moz-column-gap: normal;
    -moz-column-rule: none;
    -webkit-columns: 3;
    -webkit-column-gap: normal;
    -webkit-column-rule: none;
    columns: 3;
    column-gap: normal;
    column-rule: none;
}
```

[Back to Top](#top)

<span id="clearfix" />.clearfix()
---
Uses http://nicolasgallagher.com/micro-clearfix-hack/

Usage:
```css
.example {
    .clearfix;
}
```
Compiles to:
```css
.example {
    *zoom: 1;
}
.example:before,
.example:after {
    content: "";
    display: table;
}
.example:after {
    clear: both;
}
```

[Back to Top](#top)

<span id="linear-gradient" />.linear-gradient()
---
Simple, two-color gradient. If no background color is assigned, assigns a background-color based on a mix of start and end colors. There are a few ways to use it:
```css
.linear-gradient(#0F0, #F00);
//top to bottom gradient

.linear-gradient(#0F0, #F00, top);
//top to bottom gradient (exactly the same as the first example)

.linear-gradient(#0F0, #F00, left);
//left to right gradient

.linear-gradient(#0F0, #F00, top-diagonal)
//top left to bottom right diagonal

.linear-gradient(#0F0, #F00, bottom-diagonal)
//bottom left to top right diagonal

.linear-gradient(#0F0, #F00, 45deg);
//gradient with an angle (does not support old webkit syntax (used in iOS4))

//
//a background color (including transparent) can be added to _any_ of the above definitions:
//

.linear-gradient(#0F0, #F00, #00f);
//top to bottom gradient, with background-color of #00f

.linear-gradient(#0F0, #F00, left, #00f);
//left to right gradient with background-color of #00f

.linear-gradient(#0F0, #F00, 45deg, transparent);
//gradient with an angle with background-color of transparent
```
Example:
```css
.example {
    .linear-gradient(#0F0, #F00, transparent);
}
```
Compiles to:
```css
.example {
    background-color: transparent;
    background-image: -webkit-gradient(linear, center top, center bottom, color-stop(0, #00ff00), color-stop(0.5, #ff0000));
    background-image: -webkit-linear-gradient(270deg, #00ff00, #ff0000);
    background-image: -o-linear-gradient(270deg, #00ff00, #ff0000);
    background-image: -moz-linear-gradient(270deg, #00ff00, #ff0000);
    background-image: linear-gradient(180deg, #00ff00, #ff0000);
}
```

[Back to Top](#top)

<span id="button-gradient" />.button-gradient(@startcolor, @midcolor1, @midcolor2, @stopcolor)
---
Common button gradient style

Visual example of output: http://codepen.io/bridgestew/details/lfydn#pen-details-tab

Usage:
```css
.example {
    .button-gradient(#1e5799, #2989d8, #207cca, #7db9e8);
}
```
Compiles to:
```css
.example {
    background: -webkit-gradient(linear, center top, color-stop(0%, #1e5799), color-stop(50%, #2989d8), color-stop(51%, #207cca), color-stop(100%, #7db9e8));
    background: -webkit-linear-gradient(top, #1e5799 0%, #2989d8 50%, #207cca 51%, #7db9e8 100%);
    background: -o-linear-gradient(top, #1e5799 0%, #2989d8 50%, #207cca 51%, #7db9e8 100%);
    background: -moz-linear-gradient(top, #1e5799 0%, #2989d8 50%, #207cca 51%, #7db9e8 100%);
    background: -ms-linear-gradient(top, #1e5799 0%, #2989d8 50%, #207cca 51%, #7db9e8 100%);
    background: linear-gradient(to bottom, #1e5799 0%, #2989d8 50%, #207cca 51%, #7db9e8 100%);
}
```

[Back to Top](#top)

<span id="size" />.size(@width,@height)
---
Small mixin to set width and height. That's all it does.

Usage:
```css
.example {
    .size(34px, 200px);
}
```
Compiles to:
```css
.example {
    width: 34px;
    height: 200px;
}
```

[Back to Top](#top)

<span id="image-replacement" />.image-replacement(@width, @height, @img)
---
Using the newer Zeldman technique

http://www.zeldman.com/2012/03/01/replacing-the-9999px-hack-new-image-replacement/

Usage:
```css
.example {
    .image-replacement(100px, 200px, url(awesome.gif));
}
```
Compiles to:
```css
.example {
    background: url(url(awesome.gif)) 0 0 no-repeat;
    text-indent: 100%;
    white-space: nowrap;
    overflow: hidden;
    width: 100px;
    height: 200px;
}
```

[Back to Top](#top)

<span id="transform" />.transform(@transform) and .transform-origin(@origin)
---
Usage:
```css
.example {
    .transform(rotate(90deg));
    .transform-origin(center center);
}
```
Compiles to:
```css
.example {
    -moz-transform: rotate(90deg);
    -webkit-transform: rotate(90deg);
    -ms-transform: rotate(90deg);
    transform: rotate(90deg);
    -moz-transform-origin: center center;
    -webkit-transform-origin: center center;
    -ms-transform-origin: center center;
    transform-origin: center center;
}
```

[Back to Top](#top)

<span id="transition" />.transition(@transition)
---
Usage:
```css
.example {
    .transition(all 2s ease-in 0s);
}
```
Compiles to:
```css
.example {
    -webkit-transition: all 2s ease-in 0s;
    -moz-transition: all 2s ease-in 0s;
    -o-transition: all 2s ease-in 0s;
    -ms-transition: all 2s ease-in 0s;
    transition: all 2s ease-in 0s;
}
```