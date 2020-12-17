---
title: Why Functions
module: 12
jotted: false
---

<div class="tab">
    <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
    <button class="tablinks" onclick="openTab(event, 'Example1')">Example w/o Parameters</button>
    <button class="tablinks" onclick="openTab(event, 'Example2')">Example w/ Parameters</button>
    <button class="tablinks" onclick="openTab(event, 'Example3')">Example reuse variables</button>
    <button class="tablinks" onclick="openTab(event, 'ToDo')">To Do</button>

</div>

<div id="Overview" class="tabcontent" style="display:block">
<div class="tabhtml" markdown="1">

# Why Use Functions

To answer this question, one must look at the entire life cycle of software.  Once software written, it goes into what is called **maintenance** mode.  This means bugs are fixed, changes made, and upgrades are applied.

This accounts for over 75% of the entire life of the product!  That's a really long time.

As such, we want to minimize the amount of work that must be performed to maintain something that is "complete".  Functions help with that.

Functions:

1. Can be used over and over
2. Reduces duplicate code
3. Reduces bugs that can arise

The main goal is to reduce your overall work. Functions can help with that.

</div>
</div>

<div id="Example1" class="tabcontent" >
<div class="tabhtml" markdown="1">

## Example without a function

```js

function setup()
{
    createCanvas(600,800);
}

function draw()
{
    
    // create sum and two numbers
    var sum;
    var number1;
    var number2;

    // create another sum and two more numbers
    var sum2;
    var number3;
    var number4;

    // calculate the first sum
    number1 = 4;
    number2 = 5;    
    sum = number1 + number2;
    text("Sum: " + sum, 100, 200);

    // calculate the second sum
    number3 = 3;
    number4 = 2;
    sum2 = number3 + number4;
    text("Sum: " + sum2, 200, 200);
}
```
</div>
</div>

<div id="Example2" class="tabcontent" >
<div class="tabhtml" markdown="1">

## Example with a function

```js
function setup()
{
    createCanvas(600,800);
}
function draw()
{
    // create sum and two numbers
    var sum;
    var number1;
    var number2;

    // calculate the first sum
    number1 = 4;
    number2 = 5;    
    calculateSum(number1, number2, 100, 200); // call the calculateSum function

    // calculate the second sum
    number3 = 3;
    number4 = 2;
    calculateSum(number3, number4, 200, 200); // call the calculateSum function

    // Define the calculateSum function    
    function calculateSum(number1, number2, x, y)
    {
        sum = number1 + number2;
        text("Sum: " + sum, x, y);
    }
}
```

</div>
</div>

<div id="Example3" class="tabcontent" >
<div class="tabhtml" markdown="1">
Doesn't seem super impressive right?  What if we did it like this though?

```js
function setup()
{
    createCanvas(600,800);
}
function draw()
{
    // create sum and two numbers
    var sum;
    var number1;
    var number2;

    // calculate the first sum
    number1 = 4;
    number2 = 5;    
    calculateSum(number1, number2, 100, 200); // call calculateSum
   

    // calculate the second sum
    number1 = 3; // overwrite the number1 variable with a new value
    number2 = 2; // overwrite the number2 variable with a new value
    calculateSum(number1, number2, 200, 200); // call calculateSum
}   
    // define the calculateSum function
    function calculateSum(number1, number2, x, y)
    {
        number1 = number1 + number2;
        number2 = number1 + number2;
        sum = number1 + number2;
        text("Sum: " + sum, x, y);
    }

```

Now, the call the calculateSum function performs more actions which we no longer have to different sets of variables which makes things simpler. Additionally, the call to calculateSum doesn't change.

</div>
</div>

<div id="ToDo" class="tabcontent" >
<div class="tabhtml" markdown="1">
Try out the two different types of functions.

<iframe src="https://editor.p5js.org/" width="100%" height="800px"></iframe>
</div>
</div>