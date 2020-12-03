<h1>Some diagrams and results obtained in the experiments and conclusions on experiments</h1>

You can see below some obtained regularities (Fig.7,8).

<p align="center">
  <img src="/doc/images/norm_time_diagram.jpg"  width="500"/>
  <br>
 Fig.7. Total normalization time costs of one image pair with using the NNDR<br> method for a match search (averaged for the whole dataset)
<p>
<br>
<p align="center">
  <img src="/doc/images/expert_rates_diagram.png" width="500" />
  <br>
 Fig.8. Distribution of expert rate values by the descriptors for the SYTOSS_NURE_pngPairs100 dataset<br> (for each descriptor, it is calculated the quantity of the same values of the expert rate (ER) for each value (“0”–”4”),<br> as well as the quantity of cases where the normalization did not occur (“-1”)
<p>

The descriptors by the total normalization time TotalNormT can be ranked as follows (from faster to slower): ORB1000 < AKAZE << BRISK, SURF64 < SIFT <SURF128 << KAZE << ORB. 
Based on the mean expert assessment and its median, the descriptors can be arranged in the following order (from a higher expert rate to lower): SIFT >> SUFR128, SURF64, ORB, BRISK> KAZE> AKAZE> ORB1000. Thus, according to the experts, the SIFT descriptor has a definite advantage in the normalization quality, but it has the middle position by time consuming (Fig.7).
  
This paper didn’t have such a purpose to research descriptors under significant lighting changes, but the experiments with 3 pairs of Day_Night_pngPairs3 dataset have shown that SIFT presents the best result (all pairs have an expert rate “4”) (Fig.9), and KAZE has the lowest mean expert rate.
 
<p align="center">
  <img src="/doc/images/references.png"  />
  <br>
Fig.9. Result of SIFT based normalization for the image pair from Fig.4f (Day_Night_pngPairs3)
<p>
  
You can look through all results of our research in this repository, namely:

*	all results of experiments for SYTOSS_NURE_pngPairs100(ссылка) in (ссылка);
*	all results of experiments for Day_Night_pngPairs3(ссылка) in (ссылка);
*	all summary tables and diagrams for different scene type sets and the whole dataset [SYTOSS_NURE_pngPairs100](https://github.com/SytossResearch/DescriptorBasedNormalization/tree/master/Dataset_SYTOSS_NURE_pngPairs100) in [15] ;
*	the summary tables and diagrams for [Day_Night_pngPairs3](https://github.com/SytossResearch/DescriptorBasedNormalization/tree/master/Dataset_Day_Night_pngPairs3) for in [ссылка].

<h2>Conclutions on experiments</h2>

For the convenience of comparative descriptor analysis and making final conclusions on the work was constructed:

1. The bubble diagram (Fig.10) which clearly illustrates the number of values of the best expert rate “4” and the time costs for all descriptors, where the point size indicates the number of failed normalizations (“-1” and “0”).

<p align="center">
  <img src="/doc/images/time_cost_expert_rates_diagrams.png"  />
  <br>
Fig.10. Time costs VS expert rates of quality (the number of values “4” is on the abscissa axis, <br>the time costs value is on the ordinate axis, the point size is the number of failed normalizations (“-1” and “0”),<br> for instance, point size is 2 for SIFT and 12 for KAZE, AKAZE )
<p>
  
2. The rating diagram (Fig.11), which was made by converting values for each indicator into the 8-point rating scale. This diagram obviously presents the rating of descriptors for the considered indicators by the groups:
*	quantitative estimates NP, NMO, NI;
*	relative values Precision and Recall;
*	time costs estimates DesT, MatchT, TotalNormT (InlierT is not given because its values are too small and their effect on time costs, in general, is not significant);
*	relative quality assessments based on such expert rates: ER=”4” (the winner), ER=”-1” (absent), ER=”0” (failed) and the mean expert rate MeanER.

The diagrams 10, 11 allow to make the following conclusions:

* the descriptors AKAZE and ORB1000 have the best time costs but the least number of expert rate “4” and a high level of failed normalizations;
* the descriptors BRISK, SURF64, SIFT, SURF128 have comparable time costs and occupy an average position in time costs relative to the other descriptors, but SIFT significantly exceeds BRISK, SURF64, SURF128 in quality (a maximum number of the expert rate “4” and a minimum number of normalization failures). 
* for the SIFT algorithm, the ratio of the number of found matches to the detected points is higher than in other algorithms, i.e., SIFT detects key points and gives them a description in the best way, that makes it the winner by normalization quality among the compared algorithms. As for SURF128, SURF64, they have a similar number of key points with the SIFT algorithm, but a share of found points, which are useful for normalization, is the lowest. The normalization quality with SURF128, SURF64 is similar, like with the BRISK descriptor.
* the KAZE descriptor normalizes 1/3 longer than algorithms BRISK, SURF64, SIFT, SURF128 (but ORB does it even longer), with a maximum number of normalization failures (maximum number of the rate 
“-1”). The total number of rates “-1” and “0” is very similar for KAZE, AKAZE;
* the ORB descriptor has the most essential time costs, and the normalization quality is comparable to SURF64, SURF128, BRISK. The great ORB time costs are caused by the significant expenses on finding matches for a large number of points (the ORB algorithm finds the maximum number of key points, and only 10% of them are used for normalization).

<p align="center">
  <img src="/doc/images/8point_rating_scale_diagram.png"  />
  <br>
Fig.11. Converting all indicator values to an 8-point rating scale (point 8 is the highest mark). Each value was assigned to one of the marks from 1 to 8, depending on which interval it got into (paragraph 4.5)
<p>

  
