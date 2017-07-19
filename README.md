# **Finding Lane Lines on the Road** 

#### The goal of this project is to make a pipeline that finds lane lines on the road.

## 1. Pipeline description
My pipeline consists of the following steps:</br>
1. Read image</br>
2. Filter white color</br>
3. Convert to grayscale</br>
4. Apply blur</br>
5. Detect edges</br>
6. Extract ROI</br>
7. Detect lines</br>
8. Add lines to image</br>
</br>

When we detect lines with Hough transformation, we get a lot of line segments. In order to draw a single line on the left and right lanes, I modified the draw_lines() function to find linear equation for each lane. After that we can find intersection with top and bottom of our ROI and draw two lane lines.

## 2. Potential shortcomings
Pipeline works fine if we have clean road with solid lane lines and no other artifacts like signs, cars, etc. Also since we used linear equation for straight line we can not mark curved lane lines.

## 3. Possible improvements
I need to do research and take a look on current publications about lane line detection. New algorithms exists for line segment grouping, line prediction, etc.
