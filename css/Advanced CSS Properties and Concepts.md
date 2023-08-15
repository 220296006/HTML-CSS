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