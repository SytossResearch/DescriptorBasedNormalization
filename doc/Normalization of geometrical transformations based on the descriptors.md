<h1>Normalization of geometrical transformations based on the descriptors</h1>

The normalization algorithm used in the work consists of the following steps:

1. ***Key points search and their description with feature vectors, i.e., the descriptors, for image1 and image2*** (Fig.1,2). To define key points and their description, the work considers full-cycle algorithms (detector-descriptor algorithms), which perform both key points detection and description. The detector-descriptor algorithms SURF128, SURF64, SIFT, BRISK, ORB, ORB (1000), KAZE, AKAZE were chosen as the most perspective and interesting for normalization by the multi-source analysis. 

2. ***Definition of the correspondence between the key points on image1 and image2*** (Fig.3). To search for corresponding pairs, the Nearest Neighbor Distance Ratio (NNDR) method (modification of k-nearest neighbors, k=2) was used, and the symmetric method was covered in order to analyze some estimates of normalization.

3. ***Determination of geometric transformation parameters, which distinguishes image2 from image1*** (Fig.4). To determine these geometric transformation parameters, the RANSAC method was applied. It is designed to look for the best homography matrix without taking outliers into consideration. To be more precise, the accelerated implementation of this method supported by the OpenCV library, which was proposed in [14], was used.

4. ***Normalization of image2 to image1 (direct normalization), or normalization of image1 to image2 (inverse normalization)*** (Fig.5).  
  
  In [ссылка на полную статью], you can see more detail information about the descriptor based image normalization (with the math formulas for each step, the used program solutions for the implementation of the considered method).

<p align="center">
  <img src="/doc/images/pair.PNG" width="400" />
  <br>
  Fig.1. Pair (format: .ppm, size: 400*400)
<p>
<br>
<p align="center">
  <img src="/doc/images/keypoints.PNG" width="400"/>
  <br>
  Fig.2. The example of implementation of Step1:   <br>  the illustration of key points detection by descriptors SIFT, SURF128:   <br>а, b – key points found by SIFT detector for image1 (96 key points) and image2(104 key points), respectively;  <br> c, d – key points found by SURF128 detector for image1 (451 key points) and image2 (405 key points), respectively
<p>
<br>
<p align="center">
  <img src="/doc/images/matches1.jpg" width="400"/>
  <br>
  a
  <br>
  <img src="/doc/images/matches2.jpg" width="400"/>
  <br>
  b
  <br>
  Fig.3. The example of implementation of Step2 (the illustration of matches found with NNDR method): <br> a – SIFT; b – SURF128
<p>
<br>
<p align="center">
  <img src="/doc/images/ransac1.jpg" width="400"/>
  <br>
  a
  <br>
  <img src="/doc/images/ransac2.jpg" width="400"/>
  <br>
  b
  <br>
  Fig.4. The example of  implementation of Step3 (the illustration of inliers found with RANSAC method): <br> a – SIFT; b – SURF128
<p>
<br>
<p align="center">
  <img src="/doc/images/normalization1.jpg" width="200"/>
  <img src="/doc/images/normalization2.jpg" width="200"/>
    <br>
    a&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b
  <br>
  Fig.5. The example of implementation of Step4 (the common scene overlap as a result of direct normalization, where RED -  key points of image2 (inliers); BLUE - key points of image1 (inliers) normalized with the found direct matrix):<br>a – SIFT; b – SURF128
<p>

### More examples of normalization are here [ссылка]
### All results of normalization for the SYTOSS_NURE_pngPairs100(ссылка) dataset  are here [ссылка]
### All results of normalization for the Day_Night_pngPairs3(ссылка) dataset  are here [ссылка]

  
  


