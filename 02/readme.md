# Debug
## Problem 1
[JSFidde](https://jsfiddle.net/)
Are there any potential issues with this function? How would you test this?
```js
/**
 * Reverse a string
 */
function reverse(str) {
	return str.split('').reverse().join('');
}
let str = 'hello world';
console.log(reverse(str));
```
## Problem 2
[JSFidde](https://jsfiddle.net/)
Are there any potential issues with this function? How would you test this?
```js
/**
 * Shuffle an array
 */
function shuffle(arr) {
  for (let i = 0; i < arr.length; i++) {
    const swapIndex = Math.floor(Math.random() * arr.length)
    const curElement = arr[i]
    const cardToSwap = arr[swapIndex]
    arr[i] = cardToSwap
    arr[swapIndex] = curElement
  }
  return arr
}
let arr = [0,1,2,3,4];
shuffle(arr);
console.log(arr);
```

## Problem 3
[Processing](https://openprocessing.org/sketch/create)
Are there any potential issues with this program? How would you test this?
```js
let w = 600;
let h = 600;
let d = 20;
let r = d / 2;

let pos;

function setup() {
    createCanvas(w, h);
    pos = {
        x: Math.random() * 100 + (w / 2) - 50,
        y: Math.random() * 100 + (h / 2) - 50,
        delta: {
            x: Math.random() * 4 - 2,
            y: Math.random() * 4 - 2
        },
        color: color(Math.random() * 255, Math.random() * 255, Math.random() * 255, 165)
    }; // Set up the circle
	fill(color(0,0,0)); // Set the font to black
}

function draw() {
    noStroke(); // Set no stroke
		textSize(16); // Set text size
		text(`Math.round(${pos.x}), Math.round(${pos.y})`, 30, 30); // Print circle position
	
    fill(pos.color); // Set the color of circle to its color
    circle(pos.x, pos.y, d); // Draw circle
    pos.x += pos.delta.x; // Update x
    pos.y += pos.delta.y; // Update y

		// Bounce x
    if (pos.x - r <= 0 || pos.x + r >= w) {
        pos.delta.x *= -1;
    }
		// Bounce y
    if (pos.y - r <= 0 || pos.y + r >= w) {
        pos.delta.y *= -1;
    }
	  background(255); // Set background color
}
```