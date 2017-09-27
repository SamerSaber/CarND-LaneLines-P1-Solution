# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)



---

### Reflection

### 1.1 pipe line description

A- Convert to gray scale
B- Run Gausian Blur filter with kernel size = 5.
C- Run Canny detector to detect the edges. 
D- Determine the ROI.
E- Run Hough transform to detect the lines 
F- Averaging/Extrapolating the lines in the draw_lines() function as following.

## 1.2 draw_lines() description

A- Classification of right lines Vs left lines dependin on their slope.
B- Getting the average X and Y in both right and lef lines and consider them as a point on the line.
C- From the line equation (y = m * x + c), c can be easily calculated.
D- Using the Y values used in the top and bottom of the specified ROI we can get x = (y_avg - c)/m.
E- Hence the two lines are etermined and can be drawn.  




### 2. Identify potential shortcomings with your current pipeline

A- Not robust against brightness changes.
B- Not robust against the not needed lines appeares in the roi. 


### 3. Suggest possible improvements to your pipeline

A- Using some morphological operations (tophat for example) before canny detection to detect only lines with high contrast.
 

Another potential improvement could be to ...
