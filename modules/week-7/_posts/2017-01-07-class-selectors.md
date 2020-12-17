---
title: Class Selectors
module: 7
jotted: true
---

# Class Selectors

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'HTML')">HTML Page Example</button>
    <button class="tablinks" onclick="openTab(event, 'CSS')">Class Selectors Example</button>
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/kkFsRWlswX0" data-lity>Class Selectors Video</a></p>

<p>In the previous section, we added styles by using inline styles, embedded styles, and external style sheets.</p>

<p>In our styles, we were general to all span tags.  However, what if we wanted to find a specific tag or apply a style to several different tags?  That is where we use classes and ids in our stylesheets.  We will use stylesheets from now on.</p>

</div>

<div id="HTML" class="tabcontent">

Here's an example of an HTML page.

<div class="tabhtml" markdown="1">

```html
    <html>
        <title>Class Example</title>
        <head>
            <link rel="stylesheet" type="text/css" href="mainstyle.css">
        </head>
        <body>
            <span class="blueColor">New Color</span>
            <br>
            <span>Same Color</span>
            <br>
            <a href="http://www.amazon.com" class="blueColor">Amazon</a>
        </body>
    </html>
```

</div>

</div>

<div id="CSS" class="tabcontent">

<div class="tabhtml" markdown="1">

```css
    .blueColor{
        color:blue;
        font-family:arial;
        font-size:24px;
    }
```

</div>

<p>Notice in this example, the CSS has the name <b>.blueColor</b>.  The blueColor class identifier applies the blue color, changes the font type, and the size of the <b>span</b> tag and an <b>a</b> (anchor) tag.  They both turned blue while the other span tag without the class name did not.</p>

<p>We can get even more specific by doing something like this.</p>

<div class="tabhtml" markdown="1">

```css
    span.blueColor{
        color:blue;
        font-family:arial;
        font-size:24px;
    }
```

</div>

<p>Now, only span tags with the class <b>blueColor</b> will change.  No other tags will work.</p>

</div>