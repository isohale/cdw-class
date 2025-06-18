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

For more inforamtion on getting started with P5.js see this tutorial: https://p5js.org/tutorials/get-started/