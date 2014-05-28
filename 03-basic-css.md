### The cascade

* styles cascade from the top of a style sheet to the bottom
* styles are added or overwritten, latter takes precedence

### Specificity

* calculated using **specificity point** values: id selectors - class selectors - type selectors
* type selector: lowest 0-0-1
* class selector: medium 0-1-0
* id selector: highest 1-0-0
* three columns for selector counts
* higher specificity wins even if it appears earlier in the stylesheet

### Combining selectors

* multiple selectors can be specified
* **key selector** - rightmost, straight before the ```{```
* **prequalifiers** - all the other left to the key selector
* no space between selectors - e.g type.class not best practice (type element with class) - just use class
* specificity weights added up per selector type

### Layering styles

* use multiple classes (space separated in HTML)
* helps keeping specificity wieghts low

### Colors

* defined in the sRGB color space
* 4 ways to represent them: keywords, hexadecimal, RGB and HSL
* keywords mapped to rgb values (e.g. ```black``` is rgb(0, 0, 0))
* hexa: six character notation - 2 chars for r, g, b respectively, 0 black, f white
* [Adobe Kuler](https://kuler.adobe.com/)
* rgb() function with 3 params 0-255, 0 black, 255 white
* rgba() function, rgb + alpha 0-1 with decimal, 0 transparent, 1 opaque
* hexa was really popular, now rgba gaining popularity
* hsl() function, 3 params, not all browsers support it
* HSL: hue(0-360, color wheel degree)
* HSL: saturation(0-100%, 0 greyscale, 100 fully saturated),
* HSL: lightness(0-100%, 0 black, 100 white)
* hsla: HSL + alpha

### Lengths

* absolute or relative with different units
* pixels: ```px```, absolute, 96 pixels in an inch but exact measurement may vary
* relative: rely on the length of another measurement
* percentages: ```%```, relative, defined in relation to the length of another object, e.g. parent element
* ```em```: calculated based on an element’s font size, 1 em = element's font size pixels,
* when a font size is not explicitly stated for an element, the ```em``` unit will be relative to the font size of the closest parent element with a stated font size

