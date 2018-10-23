# VideoFill

A jQuery plugin for making a video element fill a parent or ancestor element. This is useful when trying to set a video as a background.

## Why Is This Needed?

In an ideal world HTML and CSS would be all that is required to make this work. In fact in a world that does not include the Microsoft Edge browser and only includes modern versions of Chrome, Firefox, Opera and Safari you do not need JavaScript at all and can do this with just HTML and CSS.

If you are one of the lucky ones that live in a Chrome/Firefox/Safari only world then you are in luck. Skip this plugin and just do the following for a background video that autoplays, loops and fills the entire container element that video is inside:

### HTML

```html
<div class="container-element">
  <video muted autoplay playsinline loop>
    <source src="../path-to-your-background-video.mp4">
  </video>
  <h1>Some Amazing Heading That Sits <br>On Top of Your Video</h1>
</div><!-- end container-element -->
```
