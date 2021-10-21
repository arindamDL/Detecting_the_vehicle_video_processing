### Detecting the vehicle from the video 
Detecting the vehicle from the video is a part of the Image Processing as well as Image Classification Purpose. Before the image classification of the vehicles in the video needs to separate the moving vehicles from the stationary objects. 
With the help of OpenCV library the whole video processing has done. The frames are extracted form the video and converted into Gray scal images, which is easy to preprocess the image.  
To separate (detect) the objects, it requires minimum two frames to subtract them then we get the object. If any changes (pixel value) in the next frame, after the subtraction if the pixel changes more than 30 (we consider threshold=30)
it will considered as 255 (white) and if no chnage (stationary) it will considered as 0 (black). 

  After this process, this thresholding image goes through the Morphological processing (Dilation and Erosin) to clear the detected object(if there is any balck spot on the it will remove and highlighted the white portion
  Those detected objects are considered as contour (This is a close boundary and pixels are in same level). However, some of the contours boundary look like broken. Therefore, if we use use the Hull concept to fill up those portion.
