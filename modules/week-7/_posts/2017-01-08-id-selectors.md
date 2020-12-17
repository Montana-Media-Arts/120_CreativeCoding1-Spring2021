---
title: ID Selectors
module: 7
jotted: true
---

# ID Selectors

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'HTML')">HTML Example</button>
    <button class="tablinks" onclick="openTab(event, 'CSS')">ID Selectors Example</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/Zfb_V1-lI1E" data-lity>ID Selectors Video</a></p>

<p>Another way in which we can select a tag is by their ID if they have an id attribute defined. </p>

</div>

<div id="HTML" class="tabcontent">

<p>The HTML page might look like this.</p>

<div class="tabhtml" markdown="1">

```html
    <html>
        <title>Class Example</title>
        <head>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
        <body>
            <span id="specificColor">New Color</span>
            <br>
            <span>Same Color</span>
            <br>
            <a href="http://www.amazon.com" id="specificLink">Amazon</a>
        </body>
    </html>
```

</div>

</div>

<div id="CSS" class="tabcontent">

<p>And the CSS might look like this.</p>

<div class="tabhtml" markdown="1">

```css
    #specificColor{
        color:blue;
        font-family:verdana;
        font-size:24px;
    }

    #specificLink{
        color:red;
        font-family:arial;
        font-size:28px;
    }
```

</div>

<p>This time, the color and the size of the text specific to the ID because of the <b>#</b>.</p>

</div>