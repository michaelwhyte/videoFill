# VideoFill

A jQuery plugin for making a video element fill a parent or ancestor element. This is useful when trying to set a video as a background.

## Why Is This Needed?

In an ideal world HTML and CSS would be all that is required to make a video element sit in the background and fill its container element. In fact, in a world that does not include the Microsoft Edge browser and only includes modern versions of Chrome, Firefox and Safari you do not need JavaScript at all and can do this with just HTML and CSS.

If you are one of the lucky ones that live in a Chrome/Firefox/Safari only world then you are in luck. Skip this plugin and just do the following for a background video that autoplays, loops and fills the entire container element that the video element is inside of:

### HTML

```html
<div class="container-element">
  <video muted autoplay playsinline loop class="bg-video">
    <source src="../path-to-your-background-video.mp4">
  </video>
  <h1 class="amazing-heading">Some Amazing Heading That Sits <br>On Top of Your Video</h1>
</div><!-- end container-element -->
```

### CSS

```css
.container-element {
  position: relative;
  height: 100vh; 
}

.bg-video {
  object-fit: cover;
  width: 100%;
  height: 100%;
}

/* Put your amazing heading in the middle of the container
   and on top of the video */
.amazing-heading {
  font-size: 3.6em;
  text-shadow: 2px 2px 5px black;
  text-align: center;
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```
