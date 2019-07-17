# Pixels

Once you've got an image loaded, you can manipulate its pixels. 

Pixels are stored in an one dimensional array in the variable `pixels`

The total number of elements in this pixels array is width * height of the image.

A pixel at (x, y) in the image is located at x + y * width of the image. 

### Load the pixels

Load the pixels by calling loadPixels() on your image. 
```
pImage myImage;

void setup() {
  size(500, 500)
  myImage = loadImage('my-image.gif');
}

void draw() {
  // load pixels
  myImage.loadPixels();
  // you can now access the images pixels with myImage.pixels
}
```
  
### Make changes

Make changes to the pixels by looping through and changing the color value they have stored. 

You can read the red, green, and blue values of a pixel with the red(), green(), and blue() functions. 
```
pImage myImage;

void setup() {
  size(500, 500)
  myImage = loadImage('my-image.gif');
}

void draw() {
  // load pixels
  myImage.loadPixels();
  // variable to store current pixel location in array
  int currentPixel;
  // variables to store current pixels red, green, and blue
  float currentR, currentG, currentB;
  for(var x = 0, x < myImage.width; x++) {
    for(var y = 0, y < myImage.height; y++){
      currentPixel = x + y * myImage.width;
      currentRed = red(myImage.pixels[currentPixel]);
      currentGreen = green(myImage.pixels[currentPixel]);
      currentBlue = blue(myImage.pixels[currentPixel]);
      // change the pixel value
      myImage.pixels[currentPixel] = color(currentR, currentG, currentB * 5);
    }
  }
}
```

### Update the pixels

Once you are done making changes to the pixels, you have to call updatePixels() for your changes show up.

```
pImage myImage;

void setup() {
  size(500, 500)
  myImage = loadImage('my-image.gif');
}

void draw() {
  // load pixels
  myImage.loadPixels();
  // variable to store current pixel location in array
  int currentPixel;
  // variables to store current pixels red, green, and blue
  float currentR, currentG, currentB;
  for(var x = 0, x < myImage.width; x++) {
    for(var y = 0, y < myImage.height; y++){
      currentPixel = x + y * myImage.width;
      currentRed = red(myImage.pixels[currentPixel]);
      currentGreen = green(myImage.pixels[currentPixel]);
      currentBlue = blue(myImage.pixels[currentPixel]);
      // change the pixel value
      myImage.pixels[currentPixel] = color(currentR, currentG, currentB * 5);
    }
  }
  // update pixels
  myImage.updatePixels();
  // draw image to the sketch canvas
  image(myImage, 0, 0);
}
```
