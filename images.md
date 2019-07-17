# Images

Processing has built-in data types and functions for working with images. Images should be .gif, .png, or .jpg. 

## Data type

PImage is the built-in data type for storing and working with images
```
// Variable declaration
PImage myImage;
```

## Loading images

Any images you want to use in a sketch need to be included in your sketch's data folder. Here's how you add a new file to your sketch:

1. Navigate to Sketch > Add File
2. Locate the file you want to add
3. Select the file and hit open
4. The file should now be included in your data folder. You can confim this by navigating to Sketch > Show Sketch Folder and then opening up the data folder. 

Once you've added the image, you can now load it into your sketch in the setup() function. 
```
PImage myImage;

void setup() {
  myImage = loadImage("my-new-image.gif");
}
```

## Drawing images to the screen

You can display your image in the draw() function with image()
```
// Draws myImage with the upper left corner starting at point (x, y);
image(myImage, x, y);
```

```
PImage myImage;

void setup() {
  size(500, 500);
  myImage = loadImage("my-new-image.gif");
}

void draw() {
  // this draw the image loaded above with the upper left corner starting at (0, 0)
  image(myImage, 0, 0);
}
```

You can also access the images width and height with .width and .height.
```
myImage.width
myImage.height
```

## Tint and transparency

### Tint
Allows you to set the color and transparency of an image. It works a lot like fill() and stroke() do. It accepts arguments in the same format. 
* RGB
  ```
  tint(rgb);
  ```
  where rgb is a value 0 - 255. 

* RGBA
  ```
  tint(rgb, alpha);
  ```
  where rgb is a value 0 - 255 and alpha is a value 0 - 255. Alpha allows you to control the transparency of the image (0 is completely transparent, 255 is completely opaque). If you want to just change the transparency but not the color, you can set the rgb value to white.

* Hexadecimal
  ```
  tint(#FFFFFF);
  ```
  You can also specify colors using hexadecimal. Just make sure to begin with #

* R, G, B
  ```
  tint(r, g, b);
  ```
  You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. 

* R, G, B, A
  ```
  tint(r, g, b, a);
  ```
   You can specify the r (red), g (green), and b (blue) values separately. These values run from 0 - 255. You can alsp specify the alpha value to control the transparency. This value is also 0 - 255 (0 is completely transparent, 255 is completely opaque).

### noTint

noTint() is an easy way to turn off any tint you've set previously
```
noTint();
```

## Filters

Processing has a number of built-in filters for manipulating images. 
```
filter(filterType, filterParam);
```
where filterType is:
1. GRAY - turns an image greyscale, no filterParam needed
    ```
    filter(GREY);
    ```
1. OPAQUE - turns image completely opaque, no filterParam needed
    ```
    filter(OPAQUE);
    ```
1. INVERT - inverts the value of each pixel, no filterParam needed
    ```
    filter(INVERT);
    ```
1. THRESHOLD - changes all pixels to black or white, depending on if the are above or below the threshold specified by filterParam. The threshold value should be between 0.0 and 1.0. 
    ```
    filter(THRESHOLD, 0.5);
    ```
1. POSTERIZE - limits the color channel values to the range specified by filterParam (2 - 255)
    ```
    filter(POSTERIZE, 15);
    ```
1. BLUR - applies Gaussian blue to the image with filterParam specifying how much blur
    ```
    filter(BLUR, 5);
    ```
1. ERODE - reduces light areas of image, no filterParam necessary
    ```
    filter(ERODE);
    ```
1. DILATE - increases light areas of image, no filterParam necessary
    ```
    filter(DILATE);
    ```
