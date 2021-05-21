# ComputerVisionHomeWork

The official file's name is task4_free_space_detection_without_deepLearning.ipynb


In this task we used the predicted segmentation images from task 3, then we extracted the pixels which belong to the plane.
To estimate the free space, we used ransac algorithm.            
Step 1: Compute the x and y coordinates from depth images.

Step 2: Compute the plane using x, y and z coordinates after choosing minimum 3 points from the ground plane    
Step 3: Using a pre-set distance threshold to check if numbers of inliers are satisfied     

For computing the plane, we used singular value decomposition to compute coefficients a,b and c
