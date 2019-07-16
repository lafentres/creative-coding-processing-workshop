# Text
This section is about drawing text to the sketch window and changing its color, font, and size.

## Drawing text
[Reference](https://processing.org/reference/text_.html)

* Basic text
  ```
  text("Text to draw", x, y);
  ```
  This will draw the text to the screen with the upper left corner starting at (x, y)

* Wrapping text
  ```
  text("Text to draw", x, y, width, height);
  ```
  This will draw the text to the screen with the upper left corner starting at (x, y) and a set width and height. This will wrap the text when it hits the width limit. Any text that won't fit with in the area you've defined will be cut off. 

## Changing text color
[Reference](https://processing.org/reference/fill_.html)

* RGB
  ```
  fill(rgb);
  ```
  where rgb is a value 0 - 255. 

* RGBA
  ```
  fill(rgb, alpha);
  ```
  where rgb is a value 0 - 255 and alpha is a value 0 - 255. Alpha allows you to control the transparency of the text (0 is completely transparent, 255 is completely opaque)

* Hexadecimal
  ```
  fill(#FFFFFF);
  ```
  You can also specify colors using hexadecimal. Just make sure to begin with #

* R, G, B
  ```
  fill(r, g, b);
  ```
  You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. 

* R, G, B, A
  ```
  fill(r, g, b, a);
  ```
   You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. You can alsp specify the alpha value to control the transparency. This value is also 0 - 255 (0 is completely transparent, 255 is completely opaque).

## Changing text size
[Reference](https://processing.org/reference/textSize_.html)

* Change text size with the textSize() function
  ```
  textSize(size);
  ```
  where size is an integer, representing the pixel size of the text.

## Importing and using custom fonts
[PFont Reference](https://processing.org/reference/PFont.html)

[loadFont Reference](https://processing.org/reference/loadFont_.html)

[textFont Reference](https://processing.org/reference/textFont_.html)

* Import a new font by navigating to Tools > Create Font
  * Don't set the size too small, as fonts can sometimes become blurrier as you scale them up

* Once you've clicked Ok to import the font, the font file will be placed in your current sketch's data folder.
  * You can verify this by navigating to Sketch > Show Sketch Folder and looking in the data folder. You should see a file with the extension .vlw

* Now that you've imported a font, you can use it in your sketch. 
  1. First define a variable of type PFont (Processing's built-in font class). The top of your sketch, before setup() is a good place to do this. 
      ```
      PFont customFont;
      ```
  1. Inside of setup(), load your custom font and set it
      ```
      void setup() {
        // load font
        customFont = loadFont("yourFontNameHere.vlw");
        // set font
        textFont(customFont);
      }
      ```
