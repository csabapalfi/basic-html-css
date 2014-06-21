## Backgrounds

* Backgrounds can be a solid color, an image, a gradient, or these combined.
* ```background``` - shorthand for setting background properties

### Setting background color

* background-color: accepts color values (or use background shorthand)
* transparent backgrounds (hsla, rgba) - might not be supported by all browsers, specify two background-color props, a safe fallback color first

### Setting background image

* background-image: (or background shorthand) - accepts image source identified by url() function (usual href rules, needs to be quouted)

### Background repeat

* a background image repeated indefinitely, both vertically and horizontally to fill up the element (if image is smaller)
* ```background-repeat property```: repeat, repeat-x, repeat-y, and no-repeat

### Background position

* background images are positioned in the top-left corner by default
* ```background position```: horizontal offset vertical offset
* shorthand: use one value and it'll apply both vertically and horizontally
* can also use percentages and ```top, right, bottom, left``` keywords
* 0 0 is the same as top left, 100% 0 is top right, 100% 100% is bottom right
* advantage of percentages: 50% - centering
* ```background:``` shorthand: color, image, position, repeat values - space separated

### CSS3: Gradient backgrounds

* CSS3, supported by all modern browsers
* most browser no longer require vendor prefixes for this but worth adding them just in case

### CSS3: linear gradient

* linear-gradient() function within the background or background-image property
* linear-gradient() function accepts two values: start and end color, browser takes care of transition
*  -webkit-linear-gradient() -moz-linear-gradient()
* always specify a solid fallback color before the gradient (in a separate property)
* also supports direction as first argument (degree (0-360) e.g. 45deg, or keyword e.g. ```to right bottom```)

### CSS3: radial gradient

* radial-gradient() function
* from inside to outside of an element
* paramaters include location, size, radius, and so on
* there are a number of CSS3 gradient generators to help out

### CSS3: gradient color stops

* gradient functions are like varargs
* multiple colors comma separeted at the end
* by default color stops are at equal distance but it can also be specified: color distance-in-percentage, next-color distance

### CSS3: multiple background images

* since CSS3 background or background-image accepts multiple comma separated bacgkround images
* first image comes foremost, last in the background

### CSS3: background size

*  ```background-size``` property - accepts two lengths
* ```auto``` keyword value for one of the parameters to keep aspect ratio
* percentage values are in relation to the element's size and not the image
* ```cover``` keyword value: resize background image to cover element (might be cut off)
* ``contain``` keyword value: resize to fit into the element (might not occupy the full element)

### CSS3: background clip and origin

* ```background-clip``` - surface area a background image will cover
* ```background-origin``` - where the background-position should originate
* border-box, padding-box, and content-box keyword values may be used for both of these
* background-clip: border-box by default, background image can extend into any border
* background-origin: padding-box by default, beginning of a background image can extend into the padding
