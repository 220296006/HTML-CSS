# Advanced CSS Properties and Concepts

## Styling Links With CSS

When styling links, it's important to understand how to make use of pseudo-classes to style their states effectively.

## Link states

The first thing to understand is the concept of link states — different states that links can exist in. These can be styled using different pseudo-classes:

### Link:
A link that has a destination (i.e., not just a named anchor), styled using the :link pseudo class.
Visited: A link that has already been visited (exists in the browser's history), styled using the :visited pseudo class.
Hover: A link that is hovered over by a user's mouse pointer, styled using the :hover pseudo class.

### Focus:
A link that is focused (e.g., moved to by a keyboard user using the Tab key or something similar, or programmatically focused using HTMLElement.focus()) — this is styled using the :focus pseudo class.

### Active: 
A link that is activated (e.g., clicked on), styled using the :active pseudo class.

## Inheritance in CSS

In CSS, inheritance controls what happens when no value is specified for a property on an element.

CSS properties can be categorized in two types:

inherited properties, which by default are set to the computed value of the parent element
non-inherited properties, which by default are set to initial value of the property.

## Inherited properties

When no value for an inherited property has been specified on an element, the element gets the computed value of that property on its parent element. Only the root element of the document gets the initial value given in the property's summary.

A typical example of an inherited property is the color property. Consider the following style rules and the markup:

```css

p {
    color: green;
}

```

```html

<p>This paragraph has <em>emphasized text</em> in it.</p>

```

The words "emphasized text" will appear green, since the em element has inherited the value of the color property from the p element. It does not get the initial value of the property (which is the color that is used for the root element when the page specifies no color).

Non-inherited properties
When no value for a non-inherited property has been specified on an element, the element gets the initial value of that property (as specified in the property's summary).

A typical example of a non-inherited property is the border property. Consider the following style rules and the markup:


```css

p {
  border: medium solid;
}

```

```html

<p>This paragraph has <em>emphasized text</em> in it.</p>

```

The words "emphasized text" will not have another border (since the initial value of border-style is none).

## Notes

The inherit keyword allows authors to explicitly specify inheritance. It works on both inherited and non-inherited properties.

You can control inheritance for all properties at once using the all shorthand property, which applies its value to all properties. For example:


```css

p {
  all: revert;
  font-size: 200%;
  font-weight: bold;
}

```

This reverts the style of the paragraphs' font property to the user agent's default unless a user stylesheet exists, in which case that is used instead. Then it doubles the font size and applies a font-weight of "bold".

## Overriding inheritance, an example

Using our previous example with border, if we explicitly set the inheritance with inherit, we get the following:

```css

p {
  border: medium solid;
}

em {
  border: inherit;
}

```

```html

<p>This paragraph has <em>emphasized text</em> in it.</p>

```

## Debugging CSS with Borders and Background Colors

Sometimes when writing CSS you will encounter an issue where your CSS doesn't seem to be doing what you expect. Perhaps you believe that a certain selector should match an element, but nothing happens, or a box is a different size than you expected. This article will give you guidance on how to go about debugging a CSS problem, and show you how the DevTools included in all modern browsers can help you to find out what is going on.

## How to access browser DevTools

The article What are browser developer tools is an up-to-date guide explaining how to access the tools in various browsers and platforms. While you may choose to mostly develop in a particular browser, and therefore will become most familiar with the tools included in that browser, it is worth knowing how to access them in other browsers. This will help if you are seeing different rendering between multiple browsers.

You will also find that browsers have chosen to focus on different areas when creating their DevTools. For example, in Firefox there are some excellent tools for working visually with CSS Layout, allowing you to inspect and edit Grid Layouts, Flexbox, and Shapes. However, all of the different browsers have similar fundamental tools, e.g., for inspecting the properties and values applied to elements on your page, and making changes to them from the editor.

In this lesson we will look at some useful features of the Firefox DevTools for working with CSS. In order to do so I'll be using an example file. Load this up in a new tab if you want to follow along, and open up your DevTools as described in the article linked above.

## The DOM versus view source

Something that can trip up newcomers to DevTools is the difference between what you see when you view the source of a webpage, or look at the HTML file you put on the server, and what you can see in the HTML Pane of the DevTools. While it looks roughly similar to what you can see via View Source there are some differences.

In the rendered DOM the browser may have normalized the HTML, for example by correcting some badly-written HTML for you. If you incorrectly closed an element, for instance by opening an <h2> but closing with an </h3>, the browser will figure out what you were meaning to do and the HTML in the DOM will correctly close the open <h2> with an </h2>. The DOM will also show any changes made by JavaScript.

View Source, in comparison, is the HTML source code as stored on the server. The HTML tree in your DevTools shows exactly what the browser is rendering at any given time, so it gives you an insight into what is really going on.

Inspecting the applied CSS
Select an element on your page, either by right/ctrl-clicking on it and selecting Inspect, or selecting it from the HTML tree on the left of the DevTools display. Try selecting the element with the class of box1; this is the first element on the page with a bordered box drawn around it.