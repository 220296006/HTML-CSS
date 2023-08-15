# CSS Boxes, Types and Sizes

## Understanding Type in CSS

Unattractive and poorly designed web pages bother most people and they agree that there is something undeniably wrong with the way these pages look. The two main issues are the fonts and the spacing.

## What is involved in styling text in CSS?

If you have worked with HTML or CSS already, e.g., by working through these tutorials in order, then you know that text inside an element is laid out inside the element's content box. It starts at the top left of the content area (or the top right, in the case of RTL language content), and flows towards the end of the line. Once it reaches the end, it goes down to the next line and flows to the end again. This pattern repeats until all the content has been placed in the box. Text content effectively behaves like a series of inline elements, being laid out on lines adjacent to one another, and not creating line breaks until the end of the line is reached, or unless you force a line break manually using the <br> element.

## Fonts

Let's move straight on to look at properties for styling fonts. In this example, we'll apply some CSS properties to the following HTML sample:



```html

  </head>
  <body>
    <h1>Tommy the cat</h1>

    <p>Well I remember it as though it were a meal ago...</p>

    <p>Said Tommy the Cat as he reeled back to clear whatever foreign matter may have nestled its way into his mighty throat. Many a fat alley rat had met its demise while staring point blank down the cavernous barrel of this awesome prowling machine. Truly a wonder of nature this urban predator — Tommy the cat had many a story to tell. But it was a rare occasion such as this that he did.</p>
  </body>

```

```css

      html {
        font-size: 10px;
      }

      h1 {
        font-size: 5rem;
        text-transform: capitalize;
        text-shadow: 1px 1px 1px red,
                     2px 2px 1px red;
        text-align: center;
        letter-spacing: 2px;
      }

      h1 + p {
        font-weight: bold;
      }

      p::first-line {
        letter-spacing: 4px;
        word-spacing: 4px;
      }

       p::second-line {
        letter-spacing: 4px;
        word-spacing: 4px;
      }

      p {
        font-size: 1.5rem;
        color: red;
        font-family: Helvetica, Arial, sans-serif;
        line-height: 1.6;
        letter-spacing: 1px;
      }
```
## Font families
To set a different font for your text, you use the font-family property — this allows you to specify a font (or list of fonts) for the browser to apply to the selected elements. The browser will only apply a font if it is available on the machine the website is being accessed on; if not, it will just use a browser default font. A simple example looks like so

```css

p {
  font-family: Arial;
}

```
## Color

The color property sets the color of the foreground content of the selected elements, which is usually the text, but can also include a couple of other things, such as an underline or overline placed on text using the text-decoration property.


```css

p {
  color: red;
}

```
## Understanding and Applying size in CSS

In web design, there are two types of sizing: absolute and relative. Absolute sizes, such as points or pixels, remain the same regardless of the screen size. On the other hand, relative units like percentages or R-E-M (pronounced "rem") can adjust based on the page size. When I zoom in, the font sizes using relative units scale proportionally with the rest of the page. That is why web designers often prefer using relative units for better flexibility.

According to web developers, the preferred font size unit is usually "rem." In simpler terms, 1 rem is equivalent to 16 pixels. So, if the font size is specified as 1.5 rem, you can multiply it by 16 to get the size in pixels, which would be approximately 24 pixels. Conversely, if the font size is set as 0.8 rem, it is roughly the same as 13 pixels. Luckily, you do not have to perform these calculations manually because there are numerous online calculators available for this purpose. Let's check out one of those calculators.


## Understanding the Box Model in CSS

Everything in CSS has a box around it, and understanding these boxes is key to being able to create more complex layouts with CSS, or to align items with other items. In this lesson, we will take a look at the CSS Box Model.

The CSS box model as a whole applies to block boxes and defines how the different parts of a box — margin, border, padding, and content — work together to create a box that you can see on a page. Inline boxes use just some of the behavior defined in the box model.

To add complexity, there is a standard and an alternate box model. By default, browsers use the standard box mode

## The display property

The main methods for achieving page layout in CSS all involve specifying values for the display property. This property allows us to change the default way something displays. Everything in normal flow has a default value for display; i.e., a default way that elements are set to behave. For example, the fact that paragraphs in English display one below the other is because they are styled with display: block. If you create a link around some text inside a paragraph, that link remains inline with the rest of the text, and doesn't break onto a new line. This is because the a element is display: inline by default.


### Content

 - The content of the box, where text and images appear

### Padding

 - Clears an area around the content. The padding is transparent

### Border 

- A border that goes around the padding and content
### Margin 

- Clears an area outside the border. The margin is transparent

``` css

.box {
  width: 350px;
  height: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}

```