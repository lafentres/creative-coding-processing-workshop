# Interactivity
 Processing provides simple and easy-to-use ways to make sketches interactive by using your mouse and keyboard.
 
### Mouse
 
#### Built-in variables
 1. mouseX - x coordinate of the mouse on the sketch canvas
 1. mouseY - y coordinate of the mouse on the sketch canvas
 1. pmouseX - x coordinate of the mouse on the sketch canvas from the previous frame (last time draw() ran)
 1. pmouseY - y coordinate of the mouse on the sketch canvas from the previous frame (last time draw() ran)
 1. mousePressed - true if any mouse buttons are pressed, false otherwise
 1. mouseButton - set to LEFT, CENTER, or RIGHT if mousePressed it true, represents which mouse button is currently pressed
   ```
  if(mousePressed) {
   // run code if any mouse button is pressed
  }
  
  if(mousePressed && mouseButton == RIGHT) {
   // run code if the right mouse button is being pressed
  }
  
  // draw a 50x50 rectangle with the upper left corner starting at the current mouse location
  rect(mouseX, mouseY, 50, 50);
  ```
 
#### Events
 1. mousePressed() - runs once each time a mouse button is pressed
 1. mouseReleased() - runs once each time a mouse button is released
 1. mouseMoved() - runs once each time the mouse moves
 1. mouseDragged() - runs once each time the mouse moved while a mouse button is pressed
 
 All of these events are used the same way as setup() and draw()
 ```
 void setup() {
 }
 
 void draw() {
 }
 
 void mousePressed() {
  // code to run when a mouse button is pressed
 }
 ```
 
### Keyboard
 
#### Built-in variables
 1. keyPressed - true if a keyboard key is pressed, false otherwise
 1. key - single character representing the key that has been most recently pressed or CODED if the key that was pressed was a coded key
 1. keyCode - can be ALT, CONTROL, SHIFT, UP, DOWN, LEFT, or RIGHT (for non-alphanumeric keys like alt, control, shift and arrow keys)
  ```
  if(keyPressed) {
   // run code if key is pressed
  }
  
  if(key == 'a' || key == CODED) {
   // run code if the last key pressed was 'a' or a CODED key
  }
  
  if(key == CODED && keyCode == SHIFT) {
   // run code if the last key pressed was CODED and was the shift key
  }
  ```
 
#### Events
 1. keyPressed() - runs once each time a key is pressed
 1. keyReleased() - runs once each time a key is released
 
  All of these events are used the same way as setup() and draw()
  ```
  void setup() {
  }
 
  void draw() {
  }
 
  void keyPressed() {
   // code to run when a key is pressed
  }
  ```
