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

