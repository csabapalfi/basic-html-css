## Typography

* embedded fonts allow using any font you like but important to learn about typography
* typeface is what we see, how text looks, feels, and reads, the artistic value
* font: the file containing a typeface, method of delivering artistic value

### Adding color to text

* ```color``` property
* add it to html element to set the color for all text on the page

### font-family

* which font to use
* comma separated font names, left to right fallback
* font names with multiple word to be wrapped in double quotes
* last font should be a keyword, system default font for e.g. either ```sans-serif``` or ```serif```

### font-size

* can be set using common length values

### font-style

* normal, italic, oblique, and inherit

### font-variant

* normal, small-caps, and inherit

### font-weight

* how bold is our text
* keyword values: normal, bold, bolder, lighter, and inherit
* or numeric values: 100, 200, ... 900 (from thinnest to thickest)
* normal = 400, bold = 700
* check that the font comes with a specific weight before using a value, otherwise falls back to closest

### line-height

* the distance between two lines of text (leading)
* typically just set it to 1.5 times font-size, using value 1.5 or 150%
* or if using a baseline grid might want to specify in pixels
* may also be used to vertically center text within an element (buttons, alerts, other single line text)

### shorthand

* ```font: font-style font-variant font-weight font-size/line-height font-family, font-family```
* everything optional apart from font-size and font-family

### ```:hover```

* pseudo-selector
* maybe added at the end of a selector to style when an element is in a specific state
* ```:hover``` pseudo-class styles an element when a user hovers over that

### text-align

* five values: left, right, center, justify, and inherit

### text-decoration

* none, underline, overline, line-through, and inherit
* multiple values may be specified with space separation

### text-indent

* indent first line of text
* accepts length values
* positive value indents inwards, negative outwards

### text-shadow

* length length length color
* the shadow’s horizontal offset, vertical offset, blur radius, color (opacity as well, e.g rgba)
* positive offsets right and bottom,  negative offsets left and top
* multiple shadow can be specified as comma separated
* ```box-shadow``` accepts same values plus optional fourth length: spread, + optional first value: inset

### text-transform

* changes text inline without the need for typeface variant (not like font-variant)
* values: none, capitalize, uppercase, lowercase, and inherit
* capitalize makes first letter uppercase

### letter-spacing

* adjust the space (or tracking) between the letters on the page

