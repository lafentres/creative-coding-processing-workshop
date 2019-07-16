# Shapes


## Points
[Reference](https://processing.org/reference/point_.html)

```
point(x, y);
```
Draws a point at (x, y). You can change the color of points with stroke(). You can change the size with strokeWeight().

## Lines
[Reference](https://processing.org/reference/line_.html)

```
line(x1, y1, x2, y2);
```
Draws a line between the two points (x1, y1) and (x2, y2). You can change the color of a line with stroke(). You can change the width of a line with strokeWeight().

## Quadrilaterals
[Reference](https://processing.org/reference/quad_.html)

```
quad(x1, y1, x2, y2, x3, y3, x4, y4)
```
Draws a 4 sided shape that connects the four points (x1, y1), (x2, y2), (x3, y3), and (x4, y4)

## Triangles
[Reference](https://processing.org/reference/triangle_.html)

```
triangle(x1, y1, x2, y2, x3, y3);
```
Draws a triangle that connects the three points (x1, y1), (x2, y2), and (x3, y3)

## Rectangles
[Reference](https://processing.org/reference/rect_.html)

```
rect(x, y, width, height);
```
Draws a rectangle with the upper left corner starting at (x, y).

```
rect(x, y, width, height, radius);
```
Draws a rectangle with all four corners rounded with the same radius value

```
rect(x, y, width, height, upper-left-radius, upper-right-radius, lower-right-radius, lower-left-radius);
```
Draws a rectangle with rounded corners, different radius values for each corner

## Ellipses
[Reference](https://processing.org/reference/ellipse_.html)

```
ellipse(x, y, width, height);
```
Draws an ellipse with the center at (x, y).

## Arcs
[Reference](https://processing.org/reference/arc_.html)

```
arc(x, y, width, height, start, stop);
```
Draws an arc on the ellispe defined by x, y, width and height. start and stop are in radians. Some built-in values are 0, QUARTER_PI, HALF_PI, PI, TWO_PI.

```
arc(x, y, width, height, start, stop, renderMode);
```
renderMode can be OPEN, PIE, CHORD
