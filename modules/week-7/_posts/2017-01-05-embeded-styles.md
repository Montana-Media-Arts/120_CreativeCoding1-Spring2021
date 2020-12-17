---
title: Embedded Styles
module: 7
jotted: true
---

# Adding CSS to HTML

## Embedded

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'Embedded')">Embedded Style</button>
    
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/A68gwBljCIU" data-lity>Embedded CSS Video</a></p>

<p>The second way in which we can add CSS by using <b>embedded</b> styles on the page.  By having embedded styles, we apply a format to only this page.</p>

</div>

<div id="Embedded" class="tabcontent">

<p>An example might look like this.</p>

<div class="tabhtml" markdown="1">

```html
<html>
    <title>Embedded Style Example</title>
    <head>
        <style>
            span{
                background-color:red;
            }
        </style>
    </head>
    <body>
        <span>This is the first sentence.</span>
        <br />
            This is the second sentence.
        <br />
        <span>This is the third sentence</span>
    </body>
</html>
```

</div>

<p>In this example, you see the first, and the third sentence has a background color of red. While the second sentence does not.  The style at the top of the page within the <b>&lt;head&gt;</b> tags applies the background color to all span tags.</p>

<p>What are some of the positives and negatives of using embedded styles?</p>

</div>