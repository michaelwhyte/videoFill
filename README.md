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
  height: 100vh; /* Do this if you want the element to fill the browser window...otherwise set your own height, or let any non-positioned elements inside the container to create the height of the container element...For the width, with divs, they will fill any container elements width by default due to the default display value of block. If the container is a direct child of the body, then their width will be the entire width of the browser window */
}

/* Put your amazing heading in the middle of the container */
.amazing-heading {
  
}

```
