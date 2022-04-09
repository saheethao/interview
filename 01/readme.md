# Processing 


[Processing](https://openprocessing.org/sketch/create)

Copy and paste the code below in.
```js
const r = 10;
const width = 800;
const height = 600;

function setup() {
	createCanvas(width, height); // Create the window
	frameRate(30); // Set framerate
}

function draw() {
	background(color(200, 100, 100)); // Set the background to a red color
	fill(color(255,255,255));
	textSize(60);
	text(`(${mouseX}, ${mouseY})`, 40, 60);
	noStroke(); // Have created circles have no border/stroke
	fill(color(0, 250, 0, 200)); // Have created circles be a transparent green
	circle(mouseX, mouseY, 2*r); // Draw a circle with radius r where the mouse is
	
	fill(color(0, 0, 250)); // Have created circles be a solid blue
	circle(mouseX, mouseY + 60, 2*r); // Draw a circle with radius r where the mouse is but lower
}
```

### API Reference
[Reference](https://p5js.org/reference/)
#### Functions
- [background()](https://p5js.org/reference/#/p5/background)
- [circle()](https://p5js.org/reference/#/p5/circle)
- [color()](https://p5js.org/reference/#/p5/color)
- [createCanvas()](https://p5js.org/reference/#/p5/createCanvas)
- [fill()](https://p5js.org/reference/#/p5/fill)
- [frameRate()](https://p5js.org/reference/#/p5/frameRate)
- [noStroke()](https://p5js.org/reference/#/p5/noStroke)
- [textSize()](https://p5js.org/reference/#/p5/textSize)
- [text()](https://p5js.org/reference/#/p5/text)
#### Processing Variables
- [mouseX](https://p5js.org/reference/#/p5/mouseX)
- [mouseY](https://p5js.org/reference/#/p5/mouseY)
- [windowWidth](https://p5js.org/reference/#/p5/windowWidth)
- [windowHeight](https://p5js.org/reference/#/p5/windowHeight)

## Problem 1
### Part A
Create a program which has a circle which bounces around the screen. The screen is white. The circle randomly appears near the center of screen and moves at a constant random velocity. The circle is also a random color with a transparency value of 165. When the circle reaches the border of the screen, it will bounce in the other direction.
### Part B
When the circle bounces, it must bounce at the circumference.
### Part C
When the circle is closer to the user's mouse, it's radius increases visually, but does not affect how it bounces. The growth of the radius is continuously linearly proportional to the distance of the mouse. For example when the user's mouse is within 100 pixels of the center of the circle, its radius will be its original size. It increases its radius up to 2 times the original size when it is 0 pixels away and 1.5 times the size when the mouse is 50 pixels away.
### Part D
Support up to N circles to render this animation of parts A-C
## Problem 2
### Part A
Estimate pi only using `Math.random()`, `Math.sqrt()`, and `Math.pow()` and your standard programming tools.
### Part B
Use the processing API to visualize the estimate of pi.