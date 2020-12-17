---
title: Types of Function
module: 12
jotted: false
---

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'WOParameters')">Without Parameters</button>
    <button class="tablinks" onclick="openTab(event, 'WParameters')">With Parameters</button>
   
    
</div>

<div id="Overview" class="tabcontent" style="display:block">
<div class="tabhtml" markdown="1">

# Types of functions

Besides having built-in functions and user-defined functions, there are functions with and without parameters.  They look differently when they are defined and called.   What do they look like?

</div>
</div>
<div id="WOParameters" class="tabcontent" >
<div class="tabhtml" markdown="1">

# Functions without Parameters

Recall that functions are created to combine multiple lines of code into one.  The function below creates both a circle and a square. When the function CircleSquare is called, a single circle and square are drawn to the screen in a specific location.

```js
    function CircleSquare()
    {
        circle(100,200,25);
        square(250,350,50);
    }

```
</div>
</div>
<div id="WParameters" class="tabcontent" >
<div class="tabhtml" markdown="1">

# Functions with Parameters

In the previous example, the circle and square are drawn in only one location. However, we can send in parameters to change the location of the circle and the square.

**Parameters** are variables that are passed into the function.

```js
    function CircleSquare(circleX, circleY, diameter, squareX, squareY, sideLength)
    {
        circle(circleX, circleY, diameter);
        square(squareX, squareY, sideLength);
    }
```

In the next section, let's look closer at why programmers create functions.
</div>
</div>

