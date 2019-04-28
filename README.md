# Estimating-Pi

This simple, yet intriguing program uses a Monte Carlo method to estimate the value of pi.

How does this work? The method is simple. Imagine a circle inscribed in a square.
The probability that a random point within the square is also within the circle is in fact pi/4,
since the ratio of the area of the circle to the area of the square is pi/4.
(Note that the length of one side of the square is double the length of the radius of the inscribed circle.

Area of the circle: pi * r^2
Area of the quare: (2r)^2 = 4 * r^2

# Program Details

The program is a simulation, which takes random samples of points within a virtual square, 
and determines the number of points taken that also fall within the square.

The sampling works as follows: two random values are taken, each between 0 and 1.
One represents the x coordinate, and the other represents the y coordinate.
All points necessarily fall within a virtual square bounded by the coordinates
(0, 0), (0, 1), (1, 1), and (1, 0).
If the distance from the point to the center of the square is less than the radius, or 
half of the length of the square (which is 0.5 in our case), then it also falls within the 
imaginary circle inscribed in the square.

Thus, the program holds two counters: one for the total number of points, and the other 
for the number of points that fall within the imaginary circle. Over sampling several points
the estimated value of pi becomes closer and closer to the real value.
