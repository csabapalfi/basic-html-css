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

* ```a```
