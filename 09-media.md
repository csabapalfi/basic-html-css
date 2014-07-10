## Adding media

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

## Figure caption

* ```<figcaption>``` element adds caption within a figure element
* may appear before or after media, or anywhere within figure but only once
* serves as caption for all content within the figure element
* may also be used to replace img elements alt attribute

