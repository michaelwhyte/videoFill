# VideoFill

A jQuery plugin for making a video element fill a parent or ancestor element. This is useful when trying to set a video as a background.

## Why Is This Needed?

In an ideal world HTML and CSS would be all that is required to make a video element sit in the background and fill its container element. In fact, in a world that does not include the Microsoft Edge browser and only includes modern versions of Chrome, Firefox and Safari you do not need JavaScript at all and can do this with just HTML and CSS using the CSS `object-fit` property and setting it to `cover` on the video element.

If you are one of the lucky ones that live in a Chrome/Firefox/Safari only world then you are in luck. Skip this plugin and just do the following for a background video that autoplays, loops and fills the entire container element that the video element is inside of:

### HTML Using Object-Fit

```html
<div class="container">
  <video muted autoplay playsinline loop class="bg-video">
    <source src="../path-to-your-background-video.mp4">
  </video>
  <h1 class="amazing-heading">Some Amazing Heading That Sits <br>On Top of Your Video</h1>
</div><!-- end container-element -->
```

### CSS Using Object-Fit

```css
.container {
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

## Not in a Magical Unicorn World Where all Browsers Support All the HTML/CSS Features

If you are like most web developers, you probably have to support the Edge browser. The Edge browser does support the `object-fit` property, but only for image elements. It does not support `object-fit` for HTML video elements.

To get around this limitation we can use JavaScript. In this case using JavaScript as a plugin for the jQuery library.

## How Do I Use This Thing?

This plugin and these instructions have been designed for people new to web development. Advanced users can just skip the first few steps and go to step 3

### Step 1

Download this repo by clicking on the green "Cloan or Download" button above. You can choose to "Download Zip" to download a zipped version of this plugin which you can unzip and use locally. If you want to clone it you can do that as well. The choice is yours.

If your new to all this web stuff, then just choose the "Download Zip" option.

### Step 2

Once you have downloaded this plugin to your local machine, open up the "src" folder located inside the "videoFill" folder. Inside the "src" folder you will find two files, one called "jquery.videofill.min.js" and the other called "jquery.min.js". Copy that file and paste it into your project folder (normally inside a folder called "scripts" or "js"). A common web site project folder might look something like this:

```
your-web-site-folder/
├── index.html
├── scripts/
│   ├── jquery.min.js
│   ├── jquery.videofill.min.js
```
**Note:** If you want to use the jQuery CDN copy of jQuery, then their is no need to copy the "jquery.min.js" file over to your project file. You can grab a link to the jQuery CDN file here: [code.jquery.com](https://code.jquery.com/).

If you have no idea what the jQuery CDN is, then ignore this note and move on to the next step.

### Step 3

With the JavaScript files copied over to your web site project folder, you will now need to create the HTML.

The only required HTML elements needed for this plugin to work is a container element and a video element. See the minimum suggested HTML code below:

#### HTML

```html
<div class="container">
  <video autoplay playsinline loop muted id="bg-video">
    <source src="path-to-your-video-file">
  </video>
</div><!-- end container -->
```
#### CSS

The plugin automatically generates the required CSS for you by default. Their is no need for you to set any CSS. 

If you want your container to be a certain size or other styling such as borders you are free to do so using standard CSS.

### Step 4

You will need to attach the jQuery library and the VideoFill javascript file to your HTML. Putting these before the closing body tags is the easy to fuss way to make sure it works. See the code below:

**Note:** Change the "src" attribute to the path to the required JavaScript files

#### HTML

```html
<!-- other markup above -->
<script src="path-to-the-jquery.min.js-file"></script>
<script src="path-to-the-jquery.videofill.js-file"></script>
</body>
</html>
```
### Step 5

The final step is to either create a separate JavaScript file and attach it to your HTML file and call the videoFill plugin from there or just call the videoFill() plugin from an embedded script.

For these instructions we will just call the videoFill plugin from an embedded script in the HTML. See below:

#### HTML

```html
<!-- other markup above -->
<script src="path-to-the-jquery.min.js-file"></script>
<script src="path-to-the-jquery.videofill.js-file"></script>
<script>
  $('#bg-video').videoFill();
</script>
</body>
</html>
```
**Note:** The above code snippet assumes you have a video element in the HTML that has an "id" attribute value of "bg-video". You can use any jQuery CSS selector that will select the video element that you want the VideoFill plugin to be applied to.

That's it. It should work from there.





