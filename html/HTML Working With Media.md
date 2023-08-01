# HTML Working With Media

What is Multimedia?
Multimedia comes in many different formats. It can be almost anything you can hear or see, like images, music, sound, videos, records, films, animations, and more.

Web pages often contain multimedia elements of different types and formats.

## Working With Audio

The audio element is different from the image element because it has both an opening and a closing tag. This makes it more modern and gives it more power and flexibility. Just like the image element, we use a source attribute to provide the URL of the audio file. 

<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

#### 

## The HTML video element is used to show a video on a web page.


<video width="400" controls>
  <source src="mov_bbb.mp4" type="video/mp4">
  <source src="mov_bbb.ogg" type="video/ogg">
  Your browser does not support HTML video.
</video>

<p>
Video courtesy of 
<a href="https://www.bigbuckbunny.org/" target="_blank">Big Buck Bunny</a>.
</p>

## Working With Captions and Subtitles

It is quite amazing how audio and video can be added to a website, but not everyone can always hear or understand it. Some people may be deaf, while others may have intermittent hearing or difficulty understanding content due to various other factors. Even for those who can hear, it is not always convenient to listen. 

## Embedding Media via Iframes

Embedding refers to taking content from one site and placing it within the middle of another site's page. 

There is a wide range of content that can be embedded on a page. For instance, a map from Google or Mapbox, a code demo from CodePen or Glitch, or even a slide deck from Speaker Deck or Notist. It is common practice to embed complex content from a service that handles the technical aspects. Instead of figuring out how to build a mapping service, a slide deck system, a code demo platform, or an adaptive bitrate server, you can rely on someone else's toolkit to handle all of that. Simply embed the results onto a website. So, what HTML knowledge do we need to facilitate this process?



<h2>HTML Iframes</h2>
<p>You can use the height and width attributes to specify the size of the iframe:</p>

<iframe src="demo_iframe.htm" height="200" width="300" title="Iframe Example"></iframe>

