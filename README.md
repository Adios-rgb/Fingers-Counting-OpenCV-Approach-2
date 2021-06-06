# Fingers-Counting-OpenCV-Approach-2
Detects the count of fingers in the frame using background subtraction approach.

**Functionality**

• Uses background subtraction technique to separate foreground(palm) from the background.

• Draws convex hull from palm to fingers and calculates the centroid of convex hull.

• Draws a circle from centroid(centre of palm) till the fingers.

• Counts the number of contours outside the circle(which will be fingers).

• Displays the number of fingers detected.

![image](https://user-images.githubusercontent.com/59373491/120931739-8635a980-c710-11eb-9a6d-cb3513703d23.png)

**Packages used**
• OpenCV

• Numpy

• Scikit-Learn

• time

• imutils

**Steps involved for detecting fingers**

1.	Create a ROI box where user places his hand.
2.	Apply Gaussian blur to smooth the image frame.
3.	Calculate running average for some seconds for background subtraction.
4.	Calculate absolute difference between frames and background to segment the palm and fingers and calculate maximum contour.
5.	Draw convex hull and calculate centroid from it.
6.	Calculate difference from centroid till end points (top, bottom, left, right) of convex hull. Take 80% of maximum distance as radius.
7.	Calculate circumference of circle and draw a ROI on zeros image. Use bitwise_and operation and get fingers count
8.	Display the count of fingers on the frame.

