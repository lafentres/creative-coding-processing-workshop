# Your First Sketch!
First we'll make sure Processing is installed and running correctly. Then we'll make sure printing to the console works and write your first sketch.

## Making sure Processing is running correctly
1. Open up Processing and hit the run button.
1. You should see the sketch window pop up, although it will be small and grey.
1. Close the sketch window and hit the stop button.

## Printing to the console
1. Try adding adding a line of code to print to the console
    ```
    println("Hello, Processing!");
    ```
1. Hit the run button.
   * You should see the sketch window pop up (still small and grey). If you look in your console, you should see your message print out. 
1. Close the sketch window and hit the stop button.

## Your first sketch
1. Clear out your previous code and add the following:
    ```
    // initial setup steps
    // only runs once
    void setup() {
      // set background to white
      background(255, 255, 255);
  
      // set sketch size to 500px by 500px
      size(500, 500);
    }

    // runs repeatedly, 60 times per second  
    void draw() {
      // set outline color to black
      stroke(0, 0, 0);

      // set fill color to purple/pink
      fill(255, 0, 255);
  
     // draw circles at random locations
      ellipse(int(random(100, 400)), int(random(100, 400)), 100, 100);
    }
    ```
1. Hit the run button.
    * You should see the sketch window pop up. It should have a white background and there should be circles being drawn quickly in the middle of the sketch.
1. Close the sketch window and hit stop. 
1. Go ahead and save this sketch if you'd like. 
