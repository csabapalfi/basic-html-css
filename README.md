## Basic HTML & CSS refresher

Walking through [HTML & CSS lessons from here](http://learn.shayhowe.com/html-css/)

## Why?

> Listen. Even if you think you know the answer. You might not.

## Lessons

* [1. Introduction](#intro)
* [2. Basic HTML](#basic-html)
* [3. Basic CSS](#basic-css)
* [4. The box model](#box-model)
* [5. Positioning content](#positioning)
* [6. Typography](#typography)
* [7. Backgrounds](#backgrounds)
* [8. Lists](#lists)
* [9. Media](#media)

## 1. <a name="intro"></a> Introduction

### [HTML Terms]()

* element: ```a```
* tag: ```<a>..</a>```
* attribute: e.g. href ```<a href="http://shayhowe.com/">Shay Howe</a>```

### Self closing tags

```<br> <embed> <hr> <img> <input> <link> <meta> <param> <source> <wbr>```

### Structure

doctype, head, body

```
<!DOCTYPE html>
<html lang="en">
  <head></head>
  <body></body>
</html>
```

### HTML and CSS validation

do it

### CSS Terms

* selector: p (type selector), .class, #id
* property: p { font-size: ...; }
* value: p { font-size: 16px; }

### Referencing CSS

preferably single file, in head

```
<head>
  <link rel="stylesheet" href="main.css">
</head>
```

### CSS Resets

* reset browser defaults
* has to come at the top of your CSS file
* popular: [Eric Meyer’s reset](http://meyerweb.com/eric/tools/css/reset/)
* Normalize.css - more advanced

## 2. <a name="basic-html"></a> Basic HTML

### Semantics - using the proper element

* read [this post](http://boagworld.com/dev/semantic-code-what-why-how/)
* screen readers, seo, shorter code, easier styling

### block

* block-level elements begin on a new line
* stacking one on top of the other
* occupy any available width.
* may be nested inside one another and may wrap inline-level elements
* larger pieces of content, such as paragraphs

### inline

* Inline-level elements do not begin on a new line.
* They fall into the normal flow of a document, lining up one after the other
* only maintain the width of their content.
* Inline-level elements may be nested inside one another; however, they cannot wrap block-level elements
* smaller pieces of content, such as a few words

### divs, spans

* solely for styling, no semantic value
* with class or id for layout, styling
* class or id value should not conatin styling references but meaning (e.g orange vs social)
* ```div``` block element, large groupings of content
* ```span``` inline element, smaller groupings of text

> HTML comments start with ```<!-- and end with -->.``` CSS comments start with ```/* and end with */.```

### headings

* block-level elements
* six different rankings, ```<h1>``` through ```<h6>```
* break up content and establish hierarchy
* not to increase font size!

### paragraphs

* block level
* pretty self explanatory

### ```<b>```, ```<strong>```, ```<em>```

* ```<strong>``` - strong importance
* ```<b>``` - stylistically offset
* ```<em>``` - italicize text, thereby placing emphasis on it

### building structure

* ```div```s have no semantic value, but HTML introduces structural elements
* ```<header>```, ```<nav>```, ```<article>```, ```<section>```, ```<aside>```, and ```<footer>```

### head vs header vs h1-h6

* header - structural element, outlines the heading of a segment of a page (could include a heading, introductory text, maybe even nav)
* head - not displayed on a page, outlines metadata
* h1-h6 - multiple levels of text heading throughout the page

### div vs article vs section

* div - solely stlying, no value to the outline of the document
* article - content could stand on it's own, can be redistributed indepentently
* section - thematic grouping of content

### HMTL entities

* begin with an ampersand, &, and end with a semicolon, ;
* name or numeric code between
* [copypastecharacter.com](http://copypastecharacter.com/)

### Hyperlinks

* ```a``` - anchor, link from one web page or resource to another
* inline element - but the only one which can wrap a block element (HTML5)
* href (hyperlink reference) attribute, required, specifies destination
* relative path vs absolute urls
* mailto: links, with subject, body, cc
* target="_blank" opens link a new window
* link to part of the same page: id attribute on element, then ```<a>``` with href=id-value

## 3. <a name='basic-css'></a> Basic CSS

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

## 4. <a name="box-model"></a> The box model

### ```display```

* determines how elements are displayed (block, inline and more)
* every element has a default display property value which can be overwritten
* common values are block, inline, inline-block, and none
* ```inline-block```: allow an element to behave as a block-level element (accepting all box model properties) but displayed inline with other elements
* ```none``` completely hides an element and render the page as if that element and nested elements doesn’t exist

### the box model concept

* every element on a page is a rectangular box and may have width, height, padding, borders, and margins
* the core of the box is defined by the width and height of an element
* the width and height of an element may be determined by the display property, by the contents of the element, or by specified width and height properties
* padding and then border expand the dimensions of the box outward from the element’s width and height.
* any margin we have specified will follow the border.
* each part of the box model corresponds to a CSS property: width, height, padding, border, and margin.
* total width = margin-right + border-right + padding-right + width + padding-left + border-left + margin-left
* total height = margin-top + border-top + padding-top + height + padding-bottom + border-bottom + margin-bottom

### width and height

* every element has default width and height (might be 0px)
* ```width``` and ```height``` may be specified - **but only for non-inline elements**
* **block width**: block-level elements have a default width of 100%, consuming the entire horizontal space available
* **inline width**: inline and inline-block elements expand and contract horizontally to accommodate their content
* **height**: all elements expand and contract vertically to accommodate their content
* inline-level elements cannot have a fixed size, (no width and height is accepted)

### margin and padding

* browsers have their own default margin and padding
* a CSS reset tones the default down to zero and build up our own margin and padding

### margin

* ```margin```: set the amount of space that surrounds an element
* the margin outside of any border and are completely transparent in color
* vertical margins, top and bottom, are not accepted by inline-level elements
* margins work like normal for block and inline-block elements

### padding

* provide spacing directly within an element
* falls inside of an element’s border
* padding works vertically on inline-level elements
* inline vertical padding may blend into the line above or below the given element
* padding works like normal for block and inline-block elements

### margin and padding declaration

* shorthand with 1 value: setting it on all four sides
* shorthand with 2 values: top and bottom first, then left and right
* shorthand with 4 values: top, right, bottom, and left, moving clockwise
* longhand: e.g margin-top, padding-left
* use longhand for 1 or 2 values
* use shorthand for 3 or more

### margin and padding colors

* they are completely transparent and don't accept any color values
* they show the background colors of relative elements (since they're transparent)
* margins - background color of the parent element
* padding - background color of the element the padding is applied to

### borders

* fall between the padding and margin, outline around the element
* has width, style, and color (shorthand order or border-width, etc)
* width, color: standard length and color values
* style: solid, double, dashed, dotted, and none
* indidual borders and properties can also be specified: border-top, border-left-width

### border-radius

* enables rounded corners
* accepts length units: radius by which the corners of an element are to be rounded
* one value shorthand: all corners
* two values shorthand: top-left/bottom-right and top-right/bottom-left
* four values shorthand: clockwise, starting from top-left
* longhand: e.g border-top-right-radius

### box-sizing

* additive by default
* CSS3 introduces ```box-sizing```
* values: content-box, padding-box, and border-box
* content-box: the size of an element begins with the width and height properties, and then any padding, border, or margin property values are added on from there
* padding-box: actual width, height: element width + padding (width 400 + 20 padding will be 400 px wide)
* actual width, height: element width + padding + border (width 400 + 20 padding + 5 px border will be 400 px wide)
* use border-box to make maths simpler (also helps when mixing percentages with px)
* drawback of using box-sizing: older browser don't support it


### vendor prefixes

* browsers gradually began to support different CSS3 properties and values by the way of vendor prefixes (e.g ```-webkit-box-sizing```)
*  as parts of the CSS3 specification are finalized and new browser versions are released, these vendor prefixes become less and less relevant
* Mozilla Firefox: -moz-
* Microsoft Internet Explorer: -ms-
* Webkit (Google Chrome and Apple Safari): -webkit-

### developer tools

- Chrome: Alt+Cmd+I

### universal selector

* universal selector: *  - catch-all to select all elements
* :before and :after pseudo-elements: dynamically generated with CSS

## 5. <a name="positioning"></a> Positioning content

### Positioning with Floats

* the float property allows us to take an element, remove it from the normal flow of a page
* and position it to the left or right of its parent element
* all other elements on the page will then flow around the floated element
* used on multiple elements: creating a layout by floating elements directly next to or opposite each other
* multi-column layouts can be created

### floating in practice

* common float values are: ```left``` and ```right```
* floated elements will float all the way to the edge of its parent element
* no parent: floated element floats to the edge of the page
* floated element width defaults to the width of the content within it
* use the ```width``` property to specify width
* use ```margin``` to prevent elements touching each other
* floated inline elements change their display value to block and accept width, height

### clearing & containing floats

* floats have pitfalls, originally for wrapping content around images and not layout
* styles next to a parent of a floated element might break
* margin and padding can blend into a floated element
* unwanted content can wrap around floated content

### clearing floats
* to prevent unwanted content from wrapping around floated elements, we need to clear, or contain, those floats
* clearing floats returns the page to its normal flow
* ```clear``` property, values: ```left```, ```right```, ```both```
*  left clear left floats, right clear right floats, both clears both sides
* clear property applied on an element after floated elements to return the page to it's normal flow

### containing floats (clearfix)

* effects similar to clearing (return to normal flow) but also makes sure styles are rendered correctly
* to contain floats, the floated elements must have a parent (container)
* the flow of the document will remain unaffected outside of the container
* containing everything within element with class group:

```css
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  clear: both;
  *zoom: 1;
}
```
*  :before and :after pseudo-elements
* dynamically generated elements above and below the element with the class of group
* with no content but styles to clear floats
* also known as clearfix but the class group better represents the content

### keep track of float and always clear/contain them

### positioning with inline-block

* ```display: inline-block```: placing elements next to one another within a line
* but also accepts width, height, padding, border, margin ... (as opposed to inline)
* taking full advantage of the box model without having to worry about clearing any floats


### inline block vs spaces

* inline-block elements are displayed on the same line, they also include a single space between them
* low tech, simple solution: no space between start and end tags
* another low tech solution: start HTML comment after end tag, close comment before start tag

### Creating a reusable layout

* best to write modular styles that may be reused elsewhere
* floats vs inline-block is open to debate
* one approach:  inline-block elements to create the grid—or layout—of
* and float to wrap around content (as originally intended)
* new CSS specs: watch out for ```flex-``` and ```grid-``` based properties—that

### Uniquely Positioning Elements

* precisely positioning elements: floats or inline-block might not do the job
* typically, most positioning can be handled without the use of the position property and box offset properties, but in certain cases they can be extremely helpful
* can use the ```position``` property with box offset properties
* position: how an element is positioned on a page, if it appears in the normal flow of the document
* box offset properties moving elements to ```top right bottom``` or  ```left```
* default position value is ```static```
* ```static``` means the element appears in the normal flow and doesn't accept box offset properties
* other position values are: relative and absolute

### ```position: relative```

* element appears within the normal flow a page
* leaving space for an element as intended
* also allows an element’s display position to be modified with the box offset properties
* box offset properties identify where an element will be moved from given its original position (left: 20px - pushes element to the right by 20px)

### ```position: absolute```

* element does not appear within the normal flow a page
* original space and position of the element is not preserved
* elements are moved in relation to their closest relatively positioned parent element
* should a relatively positioned parent element not exist, the element will be positioned in relation to the <body> element

## 6. <a name="typography"></a> Typography

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
* positive - further apart, negative - closer
* use relative value to ensure it works across different font sizes

### word-spacing

* spacing between words

### web safe fonts

* few fonts pre-installed on every device
* Arial
* Courier New, Courier
* Garamond
* Georgia
* Lucida Sans, Lucida Grande, Lucida
* Palatino Linotype
* Tahoma
* Times New Roman, Times
* Trebuchet
* Verdana

### embedding web fonts

* upload fonts to a server (check font lincence!)
* include them on a website via the CSS @font-face at-rule
* surround embedded font-family name with quotation marks within any CSS reference
* [Google Fonts](https://www.google.com/fonts)

```
@font-face {
  font-family: "Lobster";
  src: local("Lobster"), url("lobster.woff") format("woff");
}
```

### Quotes, citations

* ```<cite>``` - reference a creative work, author, or resource (typically title, author, URL)
* ```<q>``` -  short, inline quotations, inline
* ```<blockquote>``` -  longer external quotations, block
* q, blockquote: the browser will insert the proper quotation marks (it even respects the global lang attribute)
* q, blockquote: optional cite attribute - doesn't change appearance
* blockquote can usually include citation: both cite attrubite and cite element

## 7. <a name="backgrounds"></a> Backgrounds

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

## 8. <a name="lists"></a> Lists

HTML has 3 types of lists: unordered, ordered, and description lists

### Unordered lists

* ```<ul>``` unordered list block-level element
* ```<li>``` list items
* by default most browsers add a solid dot list item marker and margin and padding

### Ordered list

* ```<ol>``` ordered list element
* works pretty much similarly to ```<ul>``` but order matters
* by default most browser use numbers as list item markers
* ```start``` attribute on ```<ol>``` element tells where to start counting from (e.g paginated list)
* ```start``` attribute only accepts integers
* ```reversed``` boolean attribute (no value required, present=true) tells if the numbers should be in reverse order
* ```value``` attribute on an individual ```<li>``` within an ```<ol>``` changes its value within the list
* any item appearing after the one with the value is calculated accordingly

### Description lists

* description lists are used to outline multiple terms and their descriptions (e.g. glossary)
* description list block-level element, ```<dl>```
* an item consists of one or more description terms ```<dt>``` followed by one or more descriptions ```<dd>```
* in most browsers by default, the <dl> element will include vertical margins and the <dd> element includes a left margin

### Nesting lists

* always start the new list within an li and should be fine

### List style type

* the ```list-style-type``` property sets the content of a list item marker
* can change both unordedered and ordered list to anything you like
* common values: none, disc, circle, square, decimal, decimal-leading-zero, lower-roman, upper-roman, lower-greek, lower-alpha / lower-latin, upper-alpha / upper-latin

### Image as a list item marker

* set list-style-type to none
* add small backround image (0 50% no-repeat)
* add padding-left to push content right

### list-style-position

* list-style-position property can have values: inside, outside, inherit
* default is outside - no content is wrapped around the marked


### list-style shorthand

* list-style-type followed by list-style-position - space separated

### Horizontally displaying a list

* make ```<li>```s inline-block
* marker is automatically set to none
* single spaces can be removed by adding comment between lis
* inline-block is better than inline as allows specifying margins, paddings

### Floating list

* changing to inline-block or inline removes the marker
* floating keeps to marker
* need to add margin or padding to prevent markers overlapping content
* always clear or contain floats

## 9. <a name="media"></a> Adding Media

### adding images

* ```<img>``` inline element
* img element is a self-containing or empty element, single, doesn't wrap around any content
* src attribute and value must exist with a valid URL
* alt (alternative text) attribute, which describes the contents of an image
* alt text is picked up by search engines, assistive technologies and also displayed if the image can't be

### image formats

* most commonly supported formats are gif, jpg, and png
* jpg format provides quality images with high color counts but still decent file size (e.g photos)
* png format is great for images with transparencies or low color counts (e.g. icons)

### image sizing

* important to tell the browser the size of the image evene before it's loaded - so it can reserve space for it and render faster
* img tag accepts width and height attributes in HTML
* CSS width and height overrides inline width and height
* setting only width or height automatically adjusts the image size preserving aspect ratio
* setting both works as well, might distort the image
* setting width and height in HTML might have some semantic value but images usually resized in CSS

### positioning images

* by default appears in the same line as the content surrounding it (inline)
* increases the height of the line it appears to match image height
* when set to ```display: block``` then in it;s own line (as usual)
* or flush left or right (by floating - it's original purpose)
* usually need margin around a floated image (can also create a frame with background, padding)

### image element vs background image

* use ```<img>``` if image holds semantic value and relevant to the content of the page
* use background image when image is part of design or UI and not directly relevant

### adding audio

* src attribute sepcifying source URL
* requires a closing tag
* several other attributes like autoplay, controls, loop (all boolean, no value just key required, attribute names self-explanatory)
* if controls attribute is not present nothing is displayed
* preload attribute - values: none, auto (default, all data preloaded), metadata (any metadata, e.g length)

### audio types, fallbacks

* different browsers support different formats
* we can get rid of the src attribute and wrap a number of ```<source>``` elements with an audio tag
* source element have ```src``` and ```type``` (e.g. audio/ogg, audio/mpeg) attributes
* browser picks the one it recognizes
* as last fallback arbitrary HTML can be added
* media.io, mirovideoconverter for conversion

### adding video

* pretty similar to audio but with the video element
* same src, autoplay, controls, loop, preload and fallback mechanism
* displayed, even if controls is not present
* size to be specified in CSS (using width and height properties)
* poster attribute accepts an image URL to be shown before the video is played
* an additional fallback option miht be a Youtube or Vimeo iframe

### custom audio and video controls

* by default controls are browser specific
* custom look and feel can be added with javascript

### Adding inline frames

* embedding another HTML page in the current one
* iframe element, src attribute specifies the URL, may be relative to current page

### Seamless iframes

* iframe contents don't inherit styles from the page including them
* links are opened within the frame
* seamless boolean attribute changes above behaviour (but not supported by older browsers)

### Figures

* ```<figure>```, block-level, identify and wrap self-contained content, often media
* may surround image, video, etc, or multiple of those (if they form a group)
* if the figure element is moved it shouldn't disrupt the content of the page

### Figure caption

* ```<figcaption>``` element adds caption within a figure element
* may appear before or after media, or anywhere within figure but only once
* serves as caption for all content within the figure element
* may also be used to replace img elements alt attribute

