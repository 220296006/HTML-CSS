# HTML Integration

## HTML Page

HTML and all the elements, attributes, roles, and tools used to mark up content on websites or web apps have been covered. HTML plays a major role in explaining what these things are, but it is not just limited to that. HTML files are a vital part of the web. 

<!DOCTYPE html>
<html>
<head>
  <title>A Meaningful Page Title</title>
</head>
<body>

<p>The content of the body element is displayed in the browser window.</p>
<p>The content of the title element is displayed in the browser tab, in favorites and in search-engine results.</p>

</body>
</html>

## Document Head

The head element is a container for metadata (data about data) and is placed between the html tag and the body tag.

HTML metadata is data about the HTML document. Metadata is not displayed.

Metadata typically define the document title, character set, styles, scripts, and other meta information.

<!DOCTYPE html>
<html>
<head>
  <title>A Meaningful Page Title</title>
</head>
<body>

<p>The content of the body element is displayed in the browser window.</p>
<p>The content of the title element is displayed in the browser tab, in favorites and in search-engine results.</p>

</body>
</html>

## Content Structuring

1. Main
The main element is used once per webpage and tells the browser where the main content is located.

2. Header
The header and footer elements mark the header and footer areas on the page. Do not confuse header with head though. Head is where the file's metadata lives and is not displayed to users. Header is used for site headers, article headers, and headers within the content. A header is usually found at the top of most web pages and may include a logo, site name, and navigation.

3. Footer
The footer signifies that there are extra things to convey, regardless of its position on the page.

4. Article
An article often starts with a title, subtitle, author's name, and publication date, which can also be considered a header. Many web pages end with a footer at the bottom, containing links, copyright information, and additional details about the company. However, footers can also appear elsewhere. Some articles begin with metadata like hashtags or share buttons, which are suitable for a footer element. The article element wraps around any type of content unit, whether it is a long written article, a short snippet, a teaser card, a tweet, or even an app element. It represents a standalone unit of content.

5. Section
The section element is used to mark sections of content. For example, in a long essay with subheadings, each segment can be wrapped in a section element. It is also useful for dividing different topic zones on a website. Each section typically starts with its own headline.

6. Aside
Lastly, the aside element is for content that is off to the side, like sidebar information or additional details that accompany an article but are not part of its main flow. Advertisements can also be marked as an aside. Although the position on the page does not matter, the semantic meaning of these elements is crucial. The visual layout often conveys meaning, and these HTML elements help transfer that meaning from the design to the content.