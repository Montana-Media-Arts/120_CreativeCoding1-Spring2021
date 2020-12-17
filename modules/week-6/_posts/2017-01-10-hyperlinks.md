---
title: Hyperlinks
module: 6
jotted: true
---

# Hyperlinks

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'Description')">Description</button>
    
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">
<!-- video -->
<p><a href="//www.youtube.com/embed/Q4s68nncqrE" data-lity>Hyperlinks Video</a></p>

<p>Hyperlinks have been around since the beginning of HTML4 and continue today. They are the bedrock of web pages as they take us places.  They have a similar structure to image tags, and they look like this.</p>

<div class="tabhtml" markdown="1">

```html
<a href="mypage.html">Link to somewhere</a>
```

</div>

</div>

<div id="Description" class="tabcontent">

<p>The <b>&lt;a&gt;</b> tag is called the anchor tag.  It tells us that there will be a link there.  The <b>href</b> is the attribute that indicates where you are going to go.  So in the previous instance, if we clicked on the <b>Link to somewhere</b>, it would take us to the <b>mypage.html</b> page.</p>

<p>So, how does the whole page look?</p>

<div class="tabhtml" markdown="1">

```html
<html>
    <title>My first page</title>
    <body>
        <a href="secondpage.html">Go to my other page</a>
    </body>
</html>

```

</div>

<p>Whereas on the second page, you might have something that looks like this.</p>

<div class="tabhtml" markdown="1">

```html
<html>
    <title>My second page</title>
    <body>
        <a href="firstpage.html">Go to my first page</a>
    </body>
</html>

```

</div>

<p>Keep in mind that you have to have two pages named <b>secondpage.html</b> and <b>firstpage.html</b>, respectively.</p>

</div>

<p></p>

<a href='http://www.silverleaf-consulting.com/CodeEditor/' target="_new">Click here for an Interactive HTML editor</a>