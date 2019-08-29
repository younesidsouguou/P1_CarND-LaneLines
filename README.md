# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps:

1. Applying a grayscale transform since all the channels practically are same
2. Applying a gaussian blur to  get rid of noisy pixel before going through the Canny edge detection algorithm
3. Defining and applying a region of interest based on the position of our camera
4. Using Hough transform to detect straight lines in our region of interest
5. Extracting of points coordinates from Hough lines
6. Putting points form left side and right side of the image into separate arrays
7. Fitting a linear line for each array ( Left & Right ) X_coordinate = a * Y_coordinate + b
8. Based on the linear fits we predict the y coordinates givens x coordinates ot the left and right bottoms of  the image and the y coordinates of points neighboring the apex
9. Joining predicted coordinates with a line


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
