<h1>Descriptor Based Normalization</h1>

This material is intended to accompany the paper "Research of descriptor based image normalization and comparative analysis of SURF, SIFT, BRISK, ORB, KAZE, AKAZE DESCRIPTORS". The full version can be found at the link [].
It contains the own dataset with 100 image pairs, the normalized images, their overlaps, the tables with different estimations, the summary diagrams.

This work is dedicated to:
* research of the parametric normalization approach, where key points and their descriptors are used to find out the normalization parameters;
* comparing the quality and time costs of the normalization process based on different descriptors. For comparison were selected the full-cycle descriptors, such as SURF128, SURF64, SIFT, BRISK, ORB, ORB1000, KAZE, AKAZE.

<table align="center">
  <tr>
    <td align="center"><img src="/doc/images/normalization_keypoints.jpg" width="200" align="center"></td>
    <td align="left"><a href="https://github.com/SytossResearch/DescriptorBasedNormalization/blob/master/doc/Normalization%20of%20geometrical%20transformations%20based%20on%20the%20descriptors.md#normalization-of-geometrical-transformations-based-on-the-descriptors">Normalization of geometrical transformations based on the descriptors</a></td>
  </tr>
  <tr></tr>
  <tr>
    <td align="center"><img src="/doc/images/normalization_matches.jpg" width="200"  align="center"></td>
    <td align="left"><a href="https://github.com/SytossResearch/DescriptorBasedNormalization/blob/master/doc/The%20purpose%20and%20content%20of%20experiments.md#the-purpose-and-content-of-experiments">The purpose and content of experiments</a></td>
  </tr>
  <tr></tr>
  <tr>
    <td align="center"><img src="/doc/images/dataset.png" width="200"  align="center"></td>
    <td align="left"><a href="https://github.com/SytossResearch/DescriptorBasedNormalization/blob/master/doc/Dataset%20description%20for%20research%20of%20descriptor-based%20normalization.md#dataset-description-for-research-of-descriptor-based-normalization">Dataset description for research of descriptor-based normalization</a></td>
  </tr>
  <tr></tr>
  <tr>
    <td align="center"><img src="/doc/images/expert_rates_diagram.png" width="200"  align="center"></td>
    <td align="left"><a href="https://github.com/SytossResearch/DescriptorBasedNormalization/blob/master/doc/Some%20diagrams%20and%20results%20obtained%20in%20the%20experiments%20and%20conclusions%20on%20experiments.md#some-diagrams-and-results-obtained-in-the-experiments-and-conclusions-on-experiments">Some diagrams and results obtained in the experiments and conclusions on experiments</a></td>
  </tr>
  <tr></tr>
  <tr>
    <td align="center"><img src="/doc/images/conclutions.png" width="200"  align="center"></td>
    <td align="left"><a href="https://github.com/SytossResearch/DescriptorBasedNormalization/blob/master/doc/Conclusions.md#conclusions">Conclusions</a></td>
  </tr>
</table>

<h2>Repository structure</h2>

|Folder | Contains|
--- | --- 
| Dataset_SYTOSS_NURE_pngPairs100     | the description of the constructed dataset SYTOSS_NURE_pngPairs100 (Description SYTOSS_NURE100.pdf) and the dataset itself (100 image pairs as in Fig.6a–e)    
| RawDataset_SYTOSS_NURE_arw     | original raw images in ARW  
| Dataset_Day_Night_pngPairs3  | the description of the set Day_Night_pngPairs3 (Descripsion_Day_Night3.pdf) and this set itself (3 image pairs as in Fig.6f)     
| NormalizationSYTOSS_NURE_pngPairs100 | <ul> <li> the normalization results on each step for each pair  #_0.png_#_1.png:  <ul><li>**“keypoints matches”** (this folder contains the images which illustrate the key points obtained by each descriptor algorithm, the matches found with the NNDR method and the inliers found with the RANSAC method);</li> <li>**“keypoints normalization”** (this folder contains the images which illustrate the common scene overlap as a result of direct normalization and inverse normalization with the displayed key points, where RED -  key points of image2 (inliers); BLUE - key points of image1 (inliers) normalized with the found direct matrix);</li> <li>**“overlap”** (this folder contains the images which illustrate the common scene overlap as a result of direct normalization and inverse normalization)</li> </li> </ul> <li> summary results for the whole dataset  SYTOSS_NURE_pngPairs100  and all sets (DescriptionResultForSYTOSS_NURE.pdf)</li> </ul>
| NormalizationDay_Night_pngPairs3 |  <ul><li>the normalization results on each step for each pair  #_0.png_#_1.png as for NormalizationSYTOSS_NURE_pngPairs100;</li> <li>summary results for the Day_Night_pngPairs3 set  (DescriptionResultFor Day_Night.pdf)</li></ul>

<h2>References</h2>

1.	Gorokhovatskij, V.A. (2014), Strukturny\`j analiz i intellektual\`naya obrabotka danny\`kh v komp\`yuternom zrenii [Structural analysis and data mining in computer vision], Kompaniya SMIT, Khar\`kov, 316 p. (in Russian)
2.	Putyatin, E.P. and Averin, S.I. (1990), Obrabotka izobrazhenij v robototekhnike [Image processing in robotics], Mashinostroenie, Moscow, 320 p. (in Russian)
3.	Krizhevsky, A., Sutskever, I., and Hinton, G.E. (2017), ImageNet classification with deep convolutional neural networks. Communications of the ACM, No60(6), pp. 84-90. 
4.	Putjatin E.P., Jakovleva E.V., Ljubchenko V.A. (1996), “Razlozhenie matricy centroaffinnogo preobrazovanija dlja normalizacii izobrazhenij” [Centroaffine transformation matrix decomposition for image normalization], Radiojelektronika i informatika No. 4 (05), pp. 91–94. (in Russian)
5.	Yakovleva, E.V. (2004), “Metody\` odnomerny\`kh normalizaczij affinny\`kh preobrazovanij v zadachakh raspoznavaniya izobrazhenij: dissertation” [Methods of dimensional normalization affine transformations in image recognition tasks: dissertation], Kharkiv, 199 p. (in Russian)
6.	Genkin, V.L., Erosh, I.L., and Moskalev, E.S. (1988), Sistemy\` raspoznavaniya avtomatizirovanny\`kh proizvodstv [Recognition systems for automated production ], Mashinostroenie, Leningrad, 246 p. (in Russian)
7.	Lyubchenko, V.A. (2004), “Matematicheskie modeli i metody\` normalizaczii proektivny\`kh preobrazovanij v sistemakh obrabotki izobrazhenij: dissertation” [Mathematical models and methods of normalization of projective transformations in image processing systems: dissertation], Kharkiv 156 p.  
8.	Lowe, D.G. (2004), Distinctive image features from scale-invariant keypoints, International journal of computer vision, Vol. 60. – No 2. – pp. 91-110.
9.	Bay, H., Tuytelaars, T., and Van Gool, L. (2006), Surf: Speeded up robust features, European conference on computer vision. Springer, Berlin, Heidelberg, pp. 404-417. 
10.	Rublee, E. et al. (2011), ORB: An efficient alternative to SIFT or SURF, 2011 International conference on computer vision, Ieee, pp. 2564-2571. 
11.	Leutenegger, S., Chli, M., and Siegwart, R.Y. (2011), BRISK: Binary robust invariant scalable keypoints, 2011 International conference on computer vision, Ieee, pp. 2548-2555. 
12.	Alcantarilla, P.F., Bartoli, A., and Davison, A.J. (2012), KAZE features, European Conference on Computer Vision, Springer, Berlin, Heidelberg, pp. 214-227. 
13.	Alcantarilla, P. F., and Solutions, T. (2011), Fast explicit diffusion for accelerated features in nonlinear scale spaces, IEEE Trans. Patt. Anal. Mach. Intell, Vol. 34, No 7, pp. 1281-1298. 
14.	Márquez-Neila P. et al. (2016), Speeding-up homography estimation in mobile devices, Journal of Real-Time Image Processing, Vol. 11, No 1, pp. 141-154.
15.	“Detail material on “Research of descriptor based image normalization and comparative analysis of SURF, SIFT, BRISK, ORB, KAZE, AKAZE descriptors” (original image pairs, normalized images, their overlaps, the tables with different estimations, summary diagrams etc.)” available at: https://github.com/SytossResearch/DescriptorBasedNormalization (last accessed November 15, 2020).
