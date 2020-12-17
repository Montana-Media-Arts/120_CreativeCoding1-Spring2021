---
title: Math functions
module: 10
jotted: false
---

# Math functions

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Explain')">Explanation</button>
    <button class="tablinks" onclick="openTab(event, 'Example')">Example with Random</button>
    <button class="tablinks" onclick="openTab(event, 'Speed')">Add Speed</button>
    <button class="tablinks" onclick="openTab(event, 'Reference')">Reference</button>
</div>
<!-- Tab content -->
<div id="Overview" class="tabcontent" style="display:block">

<div class="tabhtml" markdown="1">

So, what is the Math function that we used before?  Random right?  When we wanted a random number, it looked like this.

```js
    number1 = Math.floor(Math.random() * 10);
```
</div>
</div>
<div id="Explain" class="tabcontent">

<div class="tabhtml" markdown="1">

Remember, the Math.random() returns a number between 0 inclusive and 1 exclusive. That means that it goes all way up to .99999999 but never gets to 1.  That is why we multiply it by some number and then use another Math function called floor, which returns the largest integer that is less than or equal to the number returned.  

For example, if you have the following.

```js
    console.log(Math.floor(3.03));
```

You will see 3.

If you have the following.

```js
    console.log(Math.floor(3.94));
```

You will also see 3.

So, we are getting a random number between 0 and 1 multiplying the number by ten, and then we get the floor to return an integer that will become our random number.

</div>
</div>

<div id="Example" class="tabcontent">

<div class="tabhtml" markdown="1">

How can we use it in our previous code?

Let's start with where we left off.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement = 13;
// this function is called only once
function setup()
{

    createCanvas(800,600);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
    circle(x,y,25);
    if(x >= 800 || x <= 0)
    {
       movement *= -1;
    }

     x += movement;
}
```

This time though, let's assign movement a random value.  To do that, we are going to assign it inside the setup function.  Now the code looks like this.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement;
// this function is called only once
function setup()
{
    createCanvas(800,600);
    movement = Math.floor(Math.random() * 10);
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
    circle(x,y,25);
    if(x >= 800 || x <= 0)
    {
       movement *= -1;
    }

     x += movement;
}
```

Now, movement will be a variable speed.  Refresh the page a few times and see if the circles move at different speeds.  It returns speeds between 0 and 9 because Math.random could return 0.  Then, if we multiply by 10, it will still be zero.  Then, if we take the floor of that, it will always be zero. Uh oh. What if I want to have at least some speed?

</div>
</div>
<div id="Speed" class="tabcontent">

<div class="tabhtml" markdown="1">

Let's change our code one more time.

```js

var redColor = 123;
var greenColor = 39;
var blueColor = 21;

var x = 100;
var y = 200;
var diameter = 50;

var movement;
// this function is called only once
function setup()
{
    createCanvas(800,600);
    movement = Math.floor(Math.random() * 10) + 1;
}
/* this function is called continuously
    while the sketch is open in the browser
*/
function draw()
{
    background(redColor,greenColor,blueColor);
    fill(255);
    circle(x,y,diameter);
    fill(redColor,greenColor,blueColor);
    circle(x,y,25);
    if(x >= 800 || x <= 0)
    {
       movement *= -1;
    }

     x += movement;
}
```

If you look at our random statement, I now add at least 1 to it.  So, if I get a zero, it will be assigned a 1, and now our range is between 1 and 10.  Try and see if it works!

There are so many more math functions at your disposal in p5.js.  Here is the link to them.  Try them out.
</div>
</div>

<div id="Reference" class="tabcontent">

<div class="tabhtml" markdown="1">

[p5.js Math Functions](https://p5js.org/reference/#group-Math)

With that, let's talk about homework for this week.
</div>
</div>
