<h1>Descriptor Based Normalization</h1>

This material is intended to accompany the paper "Research of descriptor based image normalization and comparative analysis of SURF, SIFT, BRISK, ORB, KAZE, AKAZE DESCRIPTORS". The full version can be found at the link [].
It contains the own dataset with 100 image pairs, the normalized images, their overlaps, the tables with different estimations, the summary diagrams.

This work is dedicated to:
* research of the parametric normalization approach, where key points and their descriptors are used to find out the normalization parameters;
* comparing the quality and time costs of the normalization process based on different descriptors. For comparison were selected the full-cycle descriptors, such as SURF128, SURF64, SIFT, BRISK, ORB, ORB1000, KAZE, AKAZE.

  <img src="/doc/images/normalization_keypoints.jpg" width="200" align="center">  <a href="#">Normalization of geometrical transformations based on the descriptors</a>
  <br><br>
  <img src="/doc/images/normalization_matches.jpg" width="200"  align="center"><a href="#">The purpose and content of experiments</a>
  <br><br>
  <img src="/doc/images/dataset.png" width="200"  align="center"> <a href="#">Dataset description for research of descriptor-based normalization</a>
  <br><br>
  <img src="/doc/images/expert_rates_diagram.png" width="200"  align="center"> <a href="#">Some diagrams and results obtained in the experiments and conclusions on experiments</a>
  <br><br>
  <img src="/doc/images/conclutions.png" width="200"  align="center"> <a href="#">Conclusions</a>

<h2> REPOSITORY STRUCTURE</h2>

Folder | Contains
--- | --- 
| Dataset_SYTOSS_NURE_pngPairs100     | contains the description of the constructed dataset SYTOSS_NURE_pngPairs100 (Description SYTOSS_NURE100.pdf) and the dataset itself (100 image pairs as in Fig.6a–e)    
| RawDataset_SYTOSS_NURE_arw     | contains original raw images in ARW  
| Dataset_Day_Night_pngPairs3  | contains the description of the set Day_Night_pngPairs3 (Descripsion_Day_Night3.pdf) and this set itself (3 image pairs as in Fig.6f)     
| NormalizationSYTOSS_NURE_pngPairs100 | contains: 
- the normalization results on each step for each pair  #_0.png_#_1.png: “keypoints matches” (this folder contains the images which illustrate the key points obtained by each descriptor algorithm, the matches found with the NNDR method and the inliers found with the RANSAC method);
- “keypoints normalization” (this folder contains the images which illustrate the common scene overlap as a result of direct normalization and inverse normalization with the displayed key points, where RED -  key points of image2 (inliers); BLUE - key points of image1 (inliers) normalized with the found direct matrix); 
- “overlap” (this folder contains the images which illustrate the common scene overlap as a result of direct normalization and inverse normalization) – summary results for the whole dataset  SYTOSS_NURE_pngPairs100  and all sets (DescriptionResultForSYTOSS_NURE.pdf) 
| NormalizationDay_Night_pngPairs3 | - contains: 
– the normalization results on each step for each pair  #_0.png_#_1.png as for NormalizationSYTOSS_NURE_pngPairs100;
– summary results for the Day_Night_pngPairs3 set  (DescriptionResultFor Day_Night.pdf) 

