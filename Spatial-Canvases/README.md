# Spatial Canvases 
# 2-D Canvas in p5.js
---

## 1  Setup vs Draw – the two magic blocks

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
