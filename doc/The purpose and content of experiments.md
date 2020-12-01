<h1>The purpose and content of experiments</h1>

To estimate the normalization results based on the considered descriptors, the indicators shown below were calculated for each pair.

1. **Quantitative evaluation of descriptors, precision and recall estimation (with taking found overlap):** 
    * NP – a number of found key points; NP1, NP2 – a number of found key points for image1 and image2, respectively, NPO1, NPO2 – a number of found key points on the overlap for image1 and image2, respectively; 
    * NM – a number of found matches, i.e., a number of obtained corresponding pairs of key points (NM=NI+NO); NMO – a number of matches located on the overlap;
    * NI – a number of inliers found with the RANSAC method, NO – a number of outliers discarded with the RANSAC method;
    * Precision = NI/ NM – the accuracy of finding correct matches;
    * RecallO1 = NI/ NPO1 – the completeness of inlier retrieval relative to the number of all key points on the overlap for the pattern (image1). RecallO1 ratio illustrates the usefulness of the found key points for normalization. 

2. **Estimation of time costs:**
    * DesT – the descriptor construction time (time to detect and describe key points on an image), DesT1, DesT2 – the construction time of descriptors for image1 and image2, respectively;
    * MatchT - the retrieval time of matches for an image pair;
    * InlierT – the inlier retrieval time found with the RANSAC method for an image pair;
    * avgDesT – the average time for one descriptor construction;
    * avgMatchT – the average time for one match retrieval;
    * avgInlierT – the average time for one inlier retrieval with the RANSAC method;
    * TotalNormT – total normalization time for an image pair.

3. **Expert quality assessment:**
   
   The expert rate (ER) is the expert quality assessment of normalization accuracy with a 5-point scale: “0” – normalization failed, “1” – insufficient, “2” – satisfactory, “3” – good, “4” – excellent. Value “-1” was assigned if the normalization could not be performed due to the lack of a sufficient number of matches to determine the homography matrix.

4. **Averaging the values of indicators and the rates.** The above-mentioned rates and indicators were calculated for 100 real image pairs from the SYTOSS_NURE_pngPairs100 dataset. Then for each of 5 sets (Building, Picture_outside, Picture_inside, Texture_artificial, Texture_nature), as well as for the whole dataset, the mean values were computed:

     * mean values of absolute indicators NP, NM, NI;
     * mean values of relative indicators Precision, RecallO1;
     * mean values of time costs indicators DesT; MatchT; InlierT; AvgDesT; AvgMatchT; AvgInlierT; TotalNormT;
     * the quantity of the same values of the expert rate ER for each value (“0”, “1”, “2”, “3”, “4”), as well as the amount of cases where the normalization did not occur due to the lack of inliers (values “-1”);
     * mean values of expert rates ER for each descriptor (arithmetic mean MeanER and median).

5. **Converting all indicator values from 2.4 to an 8-point rating scale.** To summarize and compare the descriptors for different indicators easier, all assessment values were converted to an 8-point scale (point 8 is the highest mark). One of the values from 1 to 8, depending on which interval it got into, was assigned to each value of the indicator. 
  
    The interval was calculated using the following formula:
  
    #### (min + i* step; min + (i+1)*step]
  
    where step=(max-min)/8, max, min – maximum and minimum values of indicator respectively, i=0,…,7. If a larger value was considered the best for an indicator, then the highest score 8 was assigned to the values from the last interval (min + 7 * step, max]. Vice versa, if a lower value was regarded as the best, then the highest score 8 was assigned to the values from the first interval [min, min + step].
