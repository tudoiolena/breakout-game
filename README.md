# Breakout Game

A classic Breakout arcade game built with vanilla JavaScript and HTML5 Canvas, created with the assistance of AI (Codeium).

## Development Process

Here's how the game was built through actual prompts and responses:

1. **Initial Setup**
   - Prompt: "This project is a breakout game. It uses JavaScript, HTML, CSS. Create an index.html file. Create a basic structure to render the game inside. This can be done using HTML and the <canvas> element. The game will be rendered entirely on the <canvas> element. The <canvas> element has an id of myCanvas and it is 480 pixels wide and 320 pixels high. Create <script> and closing </script> tags. Store a reference to the <canvas> element to the canvas variable. Create the ctx variable to store the 2D rendering context — the actual tool we can use to paint on the Canvas."
   - Action: Created HTML file with canvas setup, basic CSS styling, and initialized the 2D context for drawing.

2. **Drawing Test**
   - Prompt: "Using functions beginPath() and closePath() add a red square on the canvas, a green circle and a blue rectangle. Square and circle must be filled with color and rectangle must be colored only the outer stroke. blue color is semi transparent"
   - Action: Added test shapes to verify canvas drawing functionality with different colors and fill styles.

3. **Ball Implementation**
   - Prompt: "Define a drawBall function. This function is responsible for rendering the ball on the canvas at the current (x, y) position. Function uses the x and y variables in the arc() method to center a circle with a radius of 10. Define a draw function. This function updates the ball's position and redraws it on the canvas. Remove current Draw a red square, Draw a green circle and Draw a blue rectangle with transparent stroke as we no longer need it. Define x,y,sx,dy"
   - Action: Created ball drawing and animation functions, removed test shapes, and set up movement variables.

4. **Wall Collisions**
   - Prompt: "Check whether the ball is touching (colliding with) the wall, and if so  change the direction of its movement accordingly. There are four walls to bounce the ball off. 
   1. Check on every frame whether the ball is touching the top edge of the Canvas — if yes reverse the ball movement so it will start to move in the opposite direction and stay within the visible boundaries. Remembering that the coordinate system starts from the top left.
   If the y value of the ball position is lower than zero, change the direction of the movement on the y axis by setting it equal to itself, reversed. If the ball was moving upwards with a speed of 2 pixels per frame, now it will be moving "up" with a speed of -2 pixels, which actually equals to moving down at a speed of 2 pixels per frame. If the ball's y position is greater than the height of the Canvas (remember that we count the y values from the top left, so the top edge starts at 0 and the bottom edge is at 320 pixels, the Canvas' height), then bounce it off the bottom edge by reversing the y axis movement as before.
   2. Using example in 1 step make the same but for the ball movement left-right."
   - Action: Implemented collision detection for all walls with proper bounce mechanics.

5. **Paddle Implementation**
   - Prompt: 
      "
      1. Define a paddle to hit the ball, width of 75, height of 10  and its starting point on the x axis.
      2. Define a function that will draw the paddle on the screen.
      3. The paddle should respond to the user's actions. Implement some keyboard controls:
      Two variables for storing information on whether the left or right control button is pressed.
      Two event listeners for keydown and keyup events. We want to run some code to handle the paddle movement when the buttons are pressed.
      Two functions handling the keydown and keyup events the code that will be run when the buttons are pressed.
      The ability to move the paddle left and right
      4. Inside the draw() function check if the left or right cursor keys are pressed when each frame is rendered. If the left cursor is pressed, the paddle will move seven pixels to the left, and if the right cursor is pressed, the paddle will move seven pixels to the right."
   - Action: Added paddle with keyboard controls and movement constraints.

6. **Game over setup**
   - Prompt: "
      1. Implement game over. Instead of allowing the ball to bounce off all four walls, let's only allow three now — left, top and right. Hitting the bottom wall will end the game. If game overed, show an alert message and restart the game by reloading the page.
      2. Create some kind of collision detection between the ball and the paddle, so it can bounce off it and get back into the play area. If the ball hits the bottom edge of the Canvas we need to check whether it hits the paddle. If so, then it bounces off just like you'd expect; if not, then the game is over as before."
   - Action: Implemented brick system with proper positioning and drawing logic.

7. **Bricks Setup**
   - Prompt: "
      1. Add constants to define brickRowCount, brickColumnCount, brickWidth, brickHeight, brickPadding, const brickOffsetTop, brickOffsetLeft.
      2. Hold all bricks in a two-dimensional array. It will contain the brick columns (c), which in turn will contain the brick rows (r), which in turn will each contain an object containing the x and y position to paint each brick on the screen.
      3. Create a function drawBricks to loop through all the bricks in the array and draw them on the screen.
      4. Call the function drawBricks to see bricks"
   - Action: Added brick system with proper positioning and drawing logic.

8. **Collision Detection**
   - Prompt: "continue" (after brick implementation)
   - Action: Added collision detection for the bricks and a status property to track whether each brick has been hit.

9. **Game Enhancement**
   - Prompt: "continue"
   - Action: Added score tracking, colored bricks, and win condition.

10. **Final Features**
   - Prompt: "continue"
   - Action: Added lives system, start screen, progressive difficulty, and improved animation using requestAnimationFrame.

## Features
- Colorful brick grid with collision detection
- Responsive paddle control with arrow keys
- Score tracking system
- Three-life system
- Progressive difficulty (ball speeds up during gameplay)
- Interactive start screen
- Win/lose conditions
- Smooth animation using requestAnimationFrame
