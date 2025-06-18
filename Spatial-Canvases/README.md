# Spatial Canvases 
# 2-D Canvas in p5.js
---

## 1  Setup vs Draw 

The foundation of every p5.js sketch consists of two essential functions: `setup()` and `draw()`. These functions control when and how often your code runs, creating the basic structure for graphics and animations.

```js
function setup() {
  // Runs **once** at launch
  createCanvas(640, 480);   // prepare our 2-D canvas
}

function draw() {
  // Runs **60× a second** by default
  background(240);          // clear previous frame
  // …your drawing code here…
}

```

### Function Breakdown:

**setup() Function:**
- Executes only once when the program starts
- Used for initial setup tasks like creating the canvas, setting initial values, or loading resources
- `createCanvas(640, 480)` creates a drawing area 640 pixels wide and 480 pixels tall

**draw() Function:**
- Runs continuously (typically 60 times per second) to create animations
- Each execution represents one frame of the animation
- `background(240)` clears the canvas to a light gray color each frame, preventing trails from previous drawings
- This is where you place all your drawing commands that need to update continuously
