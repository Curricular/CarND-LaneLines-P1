


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg "Grayscale"

---
# **Finding Lane Lines on the Road** 


---

![alt text][image1]

---

## Goal
* Make a pipeline that finds lane lines on the road

---

## Pipeline

1. converted the images to grayscale
2. apply Gaussian smoothing
3. create a four sided polygon masked edge
4. apply Hough transfrom to get the lines
5. draw lines on the original image

---

## Modification to draw_line() function

1. find the average slope of proper lines for both left and right lanes
2. find the proper upper bound points
3. draw 2 lines representing left and right lanes according to slopes and points obtained from step 1 and step 2

---

## Potential shortcoming

if the lightness of the image differs a lot, the result might be slightly influenced

---

## Possible improvement
1. utilize certain statistical approaches to make the left and right lane more precise
2. eliminate the effect of lightness difference