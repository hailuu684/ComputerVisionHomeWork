# ComputerVisionHomeWork
The file's name is task4_free_space_detection_without_deepLearning.ipynb for the ransac algorithm.

Ahmed's method for this task: https://colab.research.google.com/drive/1gqOHFOklkYSH3sNHhY-mHp5OfP7z09QZ?usp=sharing( I leave this link here because the size is exceeded 100mb)

In this task, we proposed 2 methods:
1. Ransac algorithm

2. Using some transformation of Opencv( Ahmed's method to detect the freespace within the lane)



In this task we used the predicted segmentation images from task 3, then we extracted the pixels which belong to the plane.
To estimate the free space, we used ransac algorithm.            
Step 1: Compute the x and y coordinates from depth images.

Step 2: Compute the plane using x, y and z coordinates after choosing minimum 3 points from the ground plane    

Step 3: Using a pre-set distance threshold to check if numbers of inliers are satisfied     

For computing the plane, we used singular value decomposition to compute coefficients a,b and c




The summarry of Ahmed's method:

So at first I did ( Prespective transformation ) to have a birdeyeview of the road. Then a warped function to make the lines as straight as possible. Then I used some filters to do ( threshold gradinet )  so I outputted using ( SX channel, S channel, V channel and r channel ) these are all filters. Then I decided to go with the Sobel operator  ( I did create an absolute sober threshold function and magnitude threshold function  and a direction threshold function and at the end I combined the result) then I worked on the Color space (creating a HSL selection color function and had a thresholdEd S) by it a created a function that create binary output from color and gradient thresholds.
At this point I used histogram to detect lanes, And sliding window to detect the trajectory too. After all of this I made a function to calculate left and right lanes curvature .
