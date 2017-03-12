**Lane Lines P1**

[//]: # (Image References)

[image1]: ./output_images/solidWhiteCurve.jpg "White Curve"
[image2]: ./output_images/solidWhiteRight.jpg "Right"
[image3]: ./output_images/solidYellowCurve.jpg "Yellow Curve"
[image4]: ./output_images/solidYellowLeft.jpg "Yellow Left"
[video1]: ./white.mp4 "White Lanes"
[video2]: ./yellow.mp4 "Yellow Lanes"

---

###Pipeline (single images)
Main code of the project is available in the Ipython notebook `P1.ipynb` along with HTML download of the notebook `P1.html` containing examples of execution.

####1. Provide output of test images.
Following are the output of finding lanes on the set of test images in the project:
![alt text][image1]
![alt text][image2]
![alt text][image3]
![alt text][image4]

---

###Pipeline (video)

####1. Provide a link to your final video output.  

Here's a [link to my whitle lane video result](./white.mp4) and [link to my yellow lane video result](./yellow.mp4)

---
###Reflections

Finding lanes on a road was an interesting experience. It would have been helpful if I had completed an image processing course beforehand but in the end I was able to complete the project with the help of lecture notes.

I was using a too high kernel size for the Gaussian blur which resulted in affecting the output where there was an anomaly in the surface of lanes. Also, I was using too low values for threshold and line gaps in the Hough transformation of an input image resulting in shorter lines. I learned that the disadvantage of shorter lines is that they are more prone to the noise in an input image. Haing a higher threshold and long line ensures that samll anamolies are sidelined.

There are couple of flaws in the current pipeline. I think the current approach will fail on roads where the lane markings are fairly sparse due to fading over time. I see many such roads in my current city. Also, sometimes there are few sections on highway with a warning size mentioning that for next X kilometers there are strips on the road for color testing where I believe this approach will not work.

I think in such cases we will need additional sensor information like from a radar so that the car is aware about its surroundings while it plots an imaginary lane for driving.
