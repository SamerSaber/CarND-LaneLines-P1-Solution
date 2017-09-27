# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road


[//]: # (Image References)



---

### Reflection

### 1.1 pipe line description

* Convert to gray scale
* Run Gausian Blur filter with kernel size = 5.
* Run Canny detector to detect the edges. 
* Determine the ROI.
* Run Hough transform to detect the lines 
* Averaging/Extrapolating the lines in the draw_lines() function as following.

## 1.2 draw_lines() description

* Classification of right lines Vs left lines dependin on their slope.
* Getting the average X and Y in both right and lef lines and consider them as a point on the line.
* From the line equation (y = m * x + c), c can be easily calculated.
* Using the Y values used in the top and bottom of the specified ROI we can get x = (y_avg - c)/m.
* Hence the two lines are etermined and can be drawn.  




### 2. Identify potential shortcomings with your current pipeline

* Not robust against brightness changes.
* Not robust against the not needed lines appeares in the roi. 


### 3. Suggest possible improvements to your pipeline

* Using some morphological operations (tophat for example) before canny detection to detect only lines with high contrast.
 

Another potential improvement could be to ...
