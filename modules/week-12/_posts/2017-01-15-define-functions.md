---
title: Create More Functions
module: 12
jotted: true
---

# Create More Functions

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'ChangedFunction')">Changed Function</button>
    <button class="tablinks" onclick="openTab(event, 'FunctionsInFunctions')">Functions in Function</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

What about creating functions to handle keyboard interaction?  Let's start with one of the previous examples.  This sketch moves the circle based on the keyboard and a circle is created when the mouse is clicked.

```js
    
    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
    var s = 83;
    var w = 87;
    var a = 65;
    var d = 68;

    function setup() 
    {
      createCanvas(800, 600);
    }

    function draw() 
    {
      background(0);
      fill(24, 200, 29);
      circle(x, y, diameter);
    
      if (x >= 300) 
      {
        x = 50;
      }
      
      if (y >= 300) 
      {
        y = 50;
      }

      if (keyIsDown(s)) 
      {
        y += 10;
      } 
      else if (keyIsDown(w)) 
      {
        y -= 10;
      }

      if (keyIsDown(d)) 
      {
        x += 10;
      } 
      else if (keyIsDown(s)) 
      {
        x -= 10;
      }

      if (diameter < 200) 
      {
        diameter += 2;
      } 
      else if (diameter >= 200) 
      {
        diameter = 25;
      }

      ellipse(mousex, mousey, 15, 50);
     
    }

    function mousePressed() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    }

```

</div>
</div>

<div id="ChangedFunction" class="tabcontent">

<div class="tabhtml" markdown="1">

Now, let's move all the keyboard movement into a function.

```js

    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
    var s = 83;
    var w = 87;
    var a = 65;
    var d = 68;

    function setup() 
    {
      createCanvas(800, 600);
    }

    function draw() 
    {
      background(0);
      
      fill(24, 200, 29);
      circle(x, y, diameter);

      // call the function created
      controlCircle();

      ellipse(mousex, mousey, 15, 50);
     
    }

    /* This function controls all the variables of the circle */
    function controlCircle()
    {

      if (x >= 300) 
      {
        x = 50;
      }
      
      if (y >= 300) 
      {
        y = 50;
      }

      if (keyIsDown(s)) 
      {
        y += 10;
      } 
      else if (keyIsDown(w)) 
      {
        y -= 10;
      }

      if (keyIsDown(d)) 
      {
        x += 10;
      } 
      else if (keyIsDown(s)) 
      {
        x -= 10;
      }

      if (diameter < 200) 
      {
        diameter += 2;
      } 
      else if (diameter >= 200) 
      {
        diameter = 25;
      }

    }

    function mousePressed() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    }

```

What happened?  A new function named **controlCircle** handles all variable changes with the circle, including keyboard events and what do when we leave an area as well as change the size of the circle.  The controlCircle is called in the **draw** function rather than all the if statements in the draw function.  This makes things much easier to read and debug!

</div>
</div>

<div id="FunctionsInFunctions" class="tabcontent">

<div class="tabhtml" markdown="1">

We can even call a function instead of a function.  Do we do that?  Let's first define another function.

```js

    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
    var s = 83;
    var w = 87;
    var a = 65;
    var d = 68;

    function setup() 
    {
      createCanvas(800, 600);
    }

    function draw() 
    {
      background(0);
      
      fill(24, 200, 29);
      circle(x, y, diameter);

      // call the function created
      controlCircle();

      ellipse(mousex, mousey, 15, 50);
     
    }

    /* This function controls all the variables of the circle */
    function controlCircle()
    {
         if (x >= 300) 
      {
        x = 50;
      }
      
      if (y >= 300) 
      {
        y = 50;
      }

      if (keyIsDown(s)) 
      {
        y += 10;
      } 
      else if (keyIsDown(w)) 
      {
        y -= 10;
      }

      if (keyIsDown(d)) 
      {
        x += 10;
      } 
      else if (keyIsDown(a)) 
      {
        x -= 10;
      }

        
        // we call the function here.
        changeDiameter();

    }

    // This function updates the size of the circle
    function changeDiameter()
    {
        if (diameter < 200) 
        {
            diameter += 2;
        } 
        else if (diameter >= 200) 
        {
            diameter = 25;
        }

    }
    
    function mousePressed() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    
    }

```

A new function called **changeDiameter** is created, and then called inside ofthe **controlCircle** function.

Why do might one do this?  (Always a good question and you should always ask this question). It's good to separate code and make things even more readable. First, the  function **controlCircle** reduced the amount of code in the draw.  However, the code in controlCircle can be reduced as well.

 The changeDiameter function makes the controlCircle function more concise.

Finally, let's add **ConcentricCircle** function into this.

```js

    var x = 50;
    var y = 50;
    var diameter = 25;
    var mousex = 0;
    var mousey = 0;
    var s = 83;
    var w = 87;
    var a = 65;
    var d = 68;

    function setup() 
    {
      createCanvas(800, 600);
    }

    function draw() 
    {
      background(0);
      
      fill(24, 200, 29);
      circle(x, y, diameter);

      // call the function created
      controlCircle();

      ellipse(mousex, mousey, 15, 50);

      // concentric circle where x = 110 and y = 120
      ConcentricCircle(110, 120, 100, 50, 50, 120, 120, 120, 50, 120);
      // concentric circle where x = 210 and y = 220
      ConcentricCircle(210, 220, 100, 50, 50, 120, 120, 120, 50, 120);
     
    }

    /* This function controls all the variables of the circle */
    function controlCircle()
    {
         if (x >= 300) 
      {
        x = 50;
      }
      
      if (y >= 300) 
      {
        y = 50;
      }

      if (keyIsDown(s)) 
      {
        y += 10;
      } 
      else if (keyIsDown(w)) 
      {
        y -= 10;
      }

      if (keyIsDown(d)) 
      {
        x += 10;
      } 
      else if (keyIsDown(a)) 
      {
        x -= 10;
      }
  
        // we call the function here.
        changeDiameter();

    }

    // This function updates the size of the circle
    function changeDiameter()
    {
        if (diameter < 200) 
        {
            diameter += 2;
        } 
        else if (diameter >= 200) 
        {
            diameter = 25;
        }

    }
    
    function mousePressed() 
    {  
      mousex = mouseX;
      mousey = mouseY;
    
    }

    // define ConcentricCircle function
    function ConcentricCircle(x,y, outer_diameter, inner_diameter, outer_red, outer_green,outer_blue, inner_red, inner_green, inner_blue)
{
        fill(outer_red,outer_green, outer_blue);
        circle(x,y,outer_diameter);
        fill(inner_red, inner_green, inner_blue);
        circle(x,y,inner_diameter);
}

```

</div>
</div>

<div id="ToDo" class="tabcontent" >
<div class="tabhtml" markdown="1">
Try out the previous example to see how things move and view the concentric circles.

<iframe src="https://editor.p5js.org/" width="100%" height="800px"></iframe>
</div>
</div>