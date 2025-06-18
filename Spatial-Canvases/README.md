# Spatial Canvases 
## 2-D Canvas in p5.js
---

### 1  Setup vs Draw 

The foundation of every p5.js sketch consists of two essential functions: `setup()` and `draw()`. These functions control when and how often your code runs, creating the basic structure for drawing, graphics, and animations.

```js
// The setup code section runs once at launch
function setup() {
  // prepare a 2-D canvas
  // the variables define the x and y axes of the canvas
  createCanvas(640, 480);   
}

// The draw code section runs 60 frames per second 
function draw() {
  // this variable defines the background color
  background(240);
  // you add your drawing code below
}

```
For more information on getting started with p5.js see this tutorial: https://p5js.org/tutorials/get-started/

### ❌ These code snippets need to be checked
### 2  Primitives 

Basic geometric shapes are the building blocks of visual programming in p5.js. These primitive shapes can be combined to create complex designs and patterns.

```js
function setup() {
  createCanvas(640, 480);
}

function draw() {
  background(240);
  
  // rectangle: x, y, width, height
  rect(50, 50, 100, 80);
  
  // ellipse: x, y, width, height
  ellipse(200, 100, 80, 80);
  
  // line: x1, y1, x2, y2
  line(300, 50, 400, 150);
  
  // triangle: x1, y1, x2, y2, x3, y3
  triangle(450, 50, 500, 150, 550, 50);
}
```

### 3  Conditionals

Conditional statements allow your code to make decisions and respond to different situations. They enable interactive and dynamic behaviors in your sketches.

```js
function setup() {
  createCanvas(640, 480);
}

function draw() {
  background(240);
  
  // check if mouse is on the left side of the canvas
  if (mouseX < width/2) {
    // if true, draw a blue circle
    fill(0, 0, 255);
    ellipse(mouseX, mouseY, 50, 50);
  } else {
    // if false, draw a red square
    fill(255, 0, 0);
    rect(mouseX-25, mouseY-25, 50, 50);
  }
}
```

### 4  For Loops

Loops allow you to repeat code multiple times, making it efficient to create patterns, arrays of objects, or repetitive visual elements.

```js
function setup() {
  createCanvas(640, 480);
}

function draw() {
  background(240);
  
  // draw 10 circles in a row
  for (let i = 0; i < 10; i++) {
    // calculate x position for each circle
    let x = i * 60 + 30;
    // draw circle at calculated position
    ellipse(x, height/2, 40, 40);
  }
}
```

### 5  Functions

Functions allow you to organize code into reusable blocks. They help keep your code clean and make it easier to create complex behaviors.

```js
function setup() {
  createCanvas(640, 480);
}

function draw() {
  background(240);
  
  // call our custom function with parameters
  drawStar(100, 100, 30);
  drawStar(200, 200, 50);
}

// custom function to draw a star shape
function drawStar(x, y, size) {
  // draw a star at the specified position and size
  fill(255, 255, 0);
  ellipse(x, y, size, size);
  // add some details to make it look more star-like
  fill(255, 200, 0);
  ellipse(x, y, size/2, size/2);
}
```

### 6  Arrays

Arrays allow you to store multiple values in a single variable. They're useful for managing collections of objects or creating dynamic systems.

```js
// declare arrays to store multiple values
let xPositions = [100, 200, 300, 400];
let yPositions = [150, 250, 350, 450];

function setup() {
  createCanvas(640, 480);
}

function draw() {
  background(240);
  
  // loop through all positions in the arrays
  for (let i = 0; i < xPositions.length; i++) {
    // draw a circle at each stored position
    ellipse(xPositions[i], yPositions[i], 30, 30);
  }
}
```

### 7  Classes

Classes are templates for creating objects with properties and methods. They help organize complex code and create reusable object types.

```js
// define a class for creating circle objects
class Circle {
  constructor(x, y, size) {
    // initialize circle properties
    this.x = x;
    this.y = y;
    this.size = size;
    this.speed = 2;
  }
  
  // method to move the circle
  move() {
    // update x position to move circle
    this.x = this.x + this.speed;
    
    // wrap around when circle goes off screen
    if (this.x > width + this.size) {
      this.x = -this.size;
    }
  }
  
  // method to display the circle
  display() {
    // draw the circle at its current position
    ellipse(this.x, this.y, this.size, this.size);
  }
}

// create an instance of the Circle class
let myCircle;

function setup() {
  createCanvas(640, 480);
  // initialize circle object
  myCircle = new Circle(50, height/2, 40);
}

function draw() {
  background(240);
  
  // call methods on the circle object
  myCircle.move();
  myCircle.display();
}
```