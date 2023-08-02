# HTML Content Identification

## HTML Language Support 

The internet is worldwide, and people speak various languages. In HTML, there are tools to indicate the language of your content. By setting things up correctly, search engines will understand which language websites are in. Spell checkers will provide the appropriate dictionaries, and when a browser reads the content aloud, it will pronounce the words correctly. It is important for computers to know the language of the content it is processing.


<html lang="US">
<html lang="eng-gb">
<html lang="ar" dir="rtl">
<html charset="UTF-8"> 

To specify the charset in HTML, simply include a meta charset tag that equals UTF-8. Place this meta element within the head element on every page of the website, which will be explained further in the chapter eight: HTML Integrations.


## HTML Generic Elements, Div and Span

The div tag defines a division or a section in an HTML document.

The div tag is used as a container for HTML elements - which is then styled with CSS or manipulated with JavaScript.

The div tag is easily styled by using the class or id attribute.

Any sort of content can be put inside the div tag! 

<h1>The div element</h1>

<div class="myDiv">
  <h2>This is a heading in a div element</h2>
  <p>This is some text in a div element.</p>
</div>

The span tag is an inline container used to mark up a part of a text, or a part of a document.

The span tag is easily styled by CSS or manipulated with JavaScript using the class or id attribute.

The span tag is much like the div element, but diV is a block-level element and span is an inline element.


<h1>The span element</h1>

<p>My mother has <span style="color:blue;font-weight:bold">blue</span> eyes and my father has <span style="color:darkolivegreen;font-weight:bold">dark green</span> eyes.</p>
