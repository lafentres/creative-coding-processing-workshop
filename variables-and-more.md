# Variables, functions, and other useful concepts

### Data types

Processing has a few basic data types, many of which you maybe already be familiar with.

1. int - whole numbers
    ```
    // Declaration
    int a;
    int b, c;
    
    // Declaration & assignment
    int x = 10;
    
    // Reassignment
    x = 1;
    ```
1. float - decimals
    ```
    // Declaration
    float z;
    float x, y;
    
    // Declaration & assignment
    float half = 0.5;
    
    // Reassignment
    half = 1.112233;
    ```
1. char - single characters
    ```
    // Declaration
    char a;
    char b, c;
    
    // Declaration & assignment
    char letter = 'g';
    
    // Reassignment
    letter = 'p';
    ```
1. String - multiple characters
    ```
    // Declaration
    String s;
    
    // Declaration & assignment
    String sentence = "this is a sentence.";
    
    // Reassignment
    sentence = "this is a new sentence";
    ```
1. boolean - true or false
    ```
    // Declaration
    boolean isPresent;
    
    // Declaration & assignment
    boolean canMove = true;
    
    // Reassignment
    canMove = false;
    ```
1. color - colors created with the color() function
    ```
    // Declaration
    color red;
    
    // Declaration & assignment
    color blue = color(50, 100, 150);
    
    // Reassignment
    blue = color(#0000FF);
    ```
Processing also has several custom types like PFont, PImage, and more. 

### Built-in variables

Processing has a number of built-in variables available to use. We'll cover the built-in variables for mouse and key interaction later. 

Both of these are set by the call to size(). If size() isn't called, they default to 100
1. width - width of the sketch window canvas, useful for scaling sketches up/down without having to change value in a bunch of places
1. height - height of the sketch window canvas, useful for scaling sketches up/down without having to change value in a bunch of places
   ```
   println(width); // will print 100
   println(height); // will print 100
   
   size(500, 600);
   
   println(width); // will print 500
   println(height); // will print 600
   
   ellipse(width/2, height/2, width-50, height-50); // will draw a circle in the center of the sketch canvas
   ```
1. frameRate - the number of frames displayed since the sketch started running (number of times draw() has run)

### Time

Processing has several built-in functions for getting time. 

1. milis() - returns the number of milliseconds since the sketch started running
1. second() - returns current seconds as a number 0 - 59
1. minute() - returns current minute as a number 0 - 59
1. hour() - returns current hour in 24-hour format, a number 0 - 23
1. day() - returns current day of the month, a number 1 - 31
1. month() - returns current month, a number 1 - 12
1. year() - returns current year, 4 digits

### Frame Rate

By default, PRcoessing will run any code inside of draw() at a rate of 60 frames per second. You can changes this with frameRate()
```
void setup() {
  frameRate(1);
}
```

### Logic

You can use regular logical and relational operators to do comparisons between values. These include:

1. `>` - greater than 
1. `<` - less than
1. `>=` - greater than or equal to
1. `<=` - less than or equal to
1. `==` - equals
1. `!=` - does not equal
1. `&&`  - and
1. `||` - or
1. `!` - not

* if/else
```
if (true) {
  // do something
}

if (true) {
  // do something
} else {
  // do something else
}

if (true) {
  // do something
} else if (true && false) {
  // do something else
} else {
  // do something new
}
```

* for loop
```
for(int i = 0, i < 10; i++){
  // do something 10 times
}
```

### Randomness

You can get random numbers with the random() function.
```
// generates a random floating point number from 0 up to (but not including) 1
random(1);

// generates a random floating point number from 3.14 up to (but not including) 10
random(3.14, 10);

// random(5) generates a floating point number from 0 up to (but not including) 5
// which is then converted to an integer by int()
random(1);
int(random(5));
```
