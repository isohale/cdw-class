# 📐 Spatial Canvases in p5.js – A Gentle Introduction  
_Designed for students brand-new to programming & computational design_

---

## 0  Why a “spatial canvas”?

Think of the canvas as **digital tracing paper**: every frame p5.js clears the sheet and redraws shapes based on numbers in memory.  
That continuous redraw lets us animate, measure, and experiment without fear of “ruining” the original drawing.

---

## 1  Key Variables at a Glance

| Variable / Function | What it controls | Typical beginner value |
| ------------------- | ---------------- | ---------------------- |
| `createCanvas(w, h)` | **Resolution** (width & height in pixels) | `createCanvas(640, 480)` |
| `background(r, g, b)` | **Reset colour** each frame | `background(255)` (white) |
| `(0, 0)` | **Origin** – top-left corner in 2-D mode | Bottom-right is `(width, height)` |
| `rectMode(CENTER / CORNER)` | Reference point for rectangles | Default is `CORNER` |
| `colorMode(RGB / HSB)` | How numbers map to colours | Stick with RGB first |
| `frameCount` | How many frames have elapsed | Starts at 1 in `draw()` |
| `deltaTime` | ms since last frame | Good for frame-rate–independent motion |

> 📝 **Tip:** Every variable above can be logged to the console (`print(width);`) to see its live value.

---

## 2  Setup vs Draw – the two magic blocks

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
