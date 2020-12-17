---
title: HTML Forms
module: 6
jotted: true
---

# HTML Forms

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'Example')">Example</button>
    
</div>

<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<p><a href="//www.youtube.com/embed/LJ0Ldc_2B8M" data-lity>HTML Forms Video</a></p>

<p>What are HTML forms?  If you have ever purchased something online or filled out an application online or signed up for an email, your social media account, or more, you have filled out a form.  Forms are just a way for us to gather data from the end-user.  Keep in mind there are some principles to which we should adhere.</p>

<p>First, we want to adhere to standards. Use the component for their intended use.  Use checkboxes for multiple selections and radio buttons for various choices, but only one correct one.</p>

<p>Aso, use dropdown lists, use those to control the input gathered.  We are going to first focus on creating forms and what tags are required. Then, we will add a look and feel to them and add a little functionality to them.</p>

</div>

<div id="Example" class="tabcontent">

<p>Here is an example of a simple form.</p>

<div class="tabhtml" markdown="1">

```html
<html>
    <title>My first page</title>
    <body>
        
        <form action="nextPage.html" type="Post">
            First Name: <input type="text" id="fName"><br>
            Last Name: <input type="text" id="lName"><br>
            <button id="mySubmit" type="submit">Submit</button>
        </form>
    </body>
</html>

```

</div>

</div>

<p></p>

<a href='http://www.silverleaf-consulting.com/CodeEditor/' target="_new">Click here for an Interactive HTML editor</a>

Look what we did here!  We created a basic yet pretty bland form!  So, challenge yourself to add more fields. Did it work?  Great!