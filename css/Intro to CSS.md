# HTML & CSS 102

## CSS Module Focus

What is CSS?
A style sheet is like a CSS file that holds all the styles for your webpage. This adds visual appeal to your webpage. To connect the HTML and CSS, you simply link them together. HTML and CSS are closely connected and work hand-in-hand but before we dive into CSS, let's take a quick look at HTML. 

CSS, short for cascading style sheets, is the language that controls the pretty stuff on websites.

```html

<h1>My First CSS Example</h1>
<p>This is a paragraph.</p>

```

## CSS has two parts: 

The selector and the declaration block. 

## A CSS selector 

Is the first part of a CSS Rule. It is a pattern of elements and other terms that tell the browser which HTML elements should be selected to have the CSS property values inside the rule applied to them. The element or elements which are selected by the selector are referred to as the subject of the selector.


```css

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```
# CSS Declaration block

Type, class, and ID selectors
This group includes selectors that target an HTML element such as an h1 tag.

```css
 h1 {
}
```

## CSS Components

In CSS, each style declaration consists of two parts: 

A property. A value. 


```css

p {
  font-family: verdana;
}
```

## Pseudo-classes and pseudo-elements

This group of selectors includes pseudo-classes, which style certain states of an element. The :hover pseudo-class for example selects an element only when it is being hovered over by the mouse pointer:

```css

a:hover {
}

p::first-line {
}

```

## Combinators

he final group of selectors combine other selectors in order to target elements within our documents. The following, for example, selects paragraphs that are direct children of article elements using the child combinator (>):

```css

article > p {
}

```
## Specificity

Specificity is the algorithm that the browser uses to decide which property value is applied to an element. If multiple style blocks have different selectors that configure the same property with different values and target the same element, specificity decides the property value that gets applied to the element. Specificity is basically a measure of how specific a selector's selection will be:

An element selector is less specific; it will select all elements of that type that appear on a page, so it has less weight. Pseudo-element selectors have the same specificity as regular element selectors.
A class selector is more specific; it will select only the elements on a page that have a specific class attribute value, so it has more weight. Attribute selectors and pseudo-classes have the same weight as a class.

```css

.main-heading { 
    color: red; 

}


h1 { 
    color: blue; 
}
```  

```html 
<h1 class="main-heading">This is my heading.</h1>

```    


