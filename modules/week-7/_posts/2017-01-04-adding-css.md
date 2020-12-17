---
title: Adding CSS to HTML
module: 7
jotted: true
---

# Adding CSS to HTML

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
   <button class="tablinks" onclick="openTab(event, 'Inline')">Inline Style</button>
    
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p>There are three ways in which we can add CSS to an HTML page.</p>
<ol>
<li>Inline</li>
<li>Embedded</li>
<li>External</li>
</ol>
</div>

<div id="Inline" class="tabcontent">

<p><a href="//www.youtube.com/embed/ZJxsUddqZrw" data-lity>Inline CSS Video</a></p>

<p><b>Inline</b> styles are applied directly to the tag as another attribute.  Below is an example.</p>

<div class="tabhtml" markdown="1">

```html
<a href="http://www.ebay.com" style="text-decoration:none">Ebay</a>
```

</div>

<p>This style removes the underline from the link to eBay.  It is important to note that <b>style</b> only applies to this particular tag and no other tags on this page.  We will return to this point later.</p>

<p>What do we need to consider when we use inline styles? If we use inline styles and want that style on another page, we will need to duplicate the style on that page.  Not bad unless we have many pages with multiple tags that need to be changed.</p>

</div>