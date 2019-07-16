# Color

[Google's color picker](https://www.google.com/search?q=color+picker) can be super useful. You can also use the built-in color picker in Processing by navigating to Tools > Color Selector. 

## Fill and noFill
[fill Reference](https://processing.org/reference/fill_.html)

[noFill Reference](https://processing.org/reference/noFill_.html)

This is the same fill() we used on text works for filling in shapes. 

### fill()

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
   
### noFill()
  * This is an easy way to draw shapes that have no fill color (completely transparent inside)
    ```
    noFill();
    ```

## Saving colors
[Reference](https://processing.org/reference/color_.html)

* Defining colors with numbers all the time can be a little tedious, confusing, and error prone. Luckily you can save your colors as variables and use them as arguments for the fill function (and other functions that take colors)
  ```
  color myColor = color(rgb);
  ```
   
* color() accepts all the same ways of specifying color as fill()
  * RGB
    ```
    color(rgb);
    ```
    where rgb is a value 0 - 255. 

  * RGBA
    ```
    color(rgb, alpha);
    ```
    where rgb is a value 0 - 255 and alpha is a value 0 - 255. Alpha allows you to control the transparency of the color (0 is completely transparent, 255 is completely opaque)

  * Hexadecimal
    ```
    color(#FFFFFF);
    ```
    You can also specify colors using hexadecimal. Just make sure to begin with #

  * R, G, B
    ```
    color(r, g, b);
    ```
    You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. 

  * R, G, B, A
    ```
    color(r, g, b, a);
    ```
    You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. You can also specify the alpha value to control the transparency. This value is also 0 - 255 (0 is completely transparent, 255 is completely opaque).

## Outlines with stoke() and noStroke()
[stroke Reference](https://processing.org/reference/stroke_.html)

[noStroke Reference](https://processing.org/reference/noStroke_.html)

### stroke()
* This is how you change the outline/border color when drawing shapes
  ```
  stroke(rgb)
  ```
    
* stroke() accepts all the same ways of specifying color as fill()
  * RGB
    ```
    stroke(rgb);
    ```
    where rgb is a value 0 - 255. 

  * RGBA
    ```
    stroke(rgb, alpha);
    ```
    where rgb is a value 0 - 255 and alpha is a value 0 - 255. Alpha allows you to control the transparency of the outline (0 is completely transparent, 255 is completely opaque)

  * Hexadecimal
    ```
    stroke(#FFFFFF);
    ```
    You can also specify colors using hexadecimal. Just make sure to begin with #

  * R, G, B
    ```
    stroke(r, g, b);
    ```
    You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. 

  * R, G, B, A
    ```
    stroke(r, g, b, a);
    ```
    You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. You can also specify the alpha value to control the transparency. This value is also 0 - 255 (0 is completely transparent, 255 is completely opaque).

### noStoke()
  * This is an easy way to draw shapes that have no outline/border
    ```
    noStroke();
    ```

## Setting the background color
[Reference](https://processing.org/reference/background_.html)

* background() sets the color of the sketch window. You can set this just once by calling it in setup() or you can overwrite what has been drawn each time by calling it inside of draw()
  ```
  background(rgb);
  ```
  
* background() accepts all the same ways of specifying color as fill()
  * RGB
    ```
    background(rgb);
    ```
    where rgb is a value 0 - 255. 

  * RGBA
    ```
    background(rgb, alpha);
    ```
    where rgb is a value 0 - 255 and alpha is a value 0 - 255. Alpha allows you to control the transparency of the background (0 is completely transparent, 255 is completely opaque)

  * Hexadecimal
    ```
    background(#FFFFFF);
    ```
    You can also specify colors using hexadecimal. Just make sure to begin with #

  * R, G, B
    ```
    background(r, g, b);
    ```
    You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. 

  * R, G, B, A
    ```
    backgroud(r, g, b, a);
    ```
    You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. You can also specify the alpha value to control the transparency. This value is also 0 - 255 (0 is completely transparent, 255 is completely opaque).  
