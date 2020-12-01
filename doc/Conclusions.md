<h1>Conclusions</h1>

The following conclusions as to the result of the research:

*	all descriptors can be used for normalization;
*	the SIFT algorithm presented the best quality (even at an extreme change of lighting), however, SIFT time costs occupy an average position, along with SURF, BRISK which are significantly inferior to it by quality;
*	the fastest algorithms were ORB1000 and AKAZE, the normalization quality with them is lower than with other algorithms;
*	the KAZE algorithm is slower (only ORB is even more slower) and inferior to SIFT, SURF, BRISK, ORB in quality;
*	the ORB descriptor has the most substantial time costs and averaged quality comparable to SURF and BRISK;
*	SURF64 and SURF128 descriptors showed comparable quality and time costs, SURF64 is faster, SURF128 has better quality, but these differences are insignificant;
*	the worst results were obtained for texture images;
*	the symmetric method usage for searching matches at the 2nd step doubles the time costs of the normalization process in general.

Therefore, it is recommended to use the SIFT descriptor for general tasks where it is necessary to process images with the scenes, which are similar to ones of the dataset SYTOSS_NURE_pngPairs100, and the time costs requirement is not critical.  If time costs are paramount and quality can be neglected within reasonable limits, it is better to use binary descriptors ORB1000 or AKAZE.

Findings on the paper are based on the image normalization of the SYTOSS_NURE_pngPairs100 dataset, which contains image scenes of different types, 40% of which are images of natural and artificial textures. As the normalization of images of this type showed the worst results, the conclusions for the other sets may differ slightly.

In this work, the expert rates were applied to assess the normalization quality because a person can match images after normalization in the best way, but this approach to estimation is very time-costuming and is not devoid of subjectivity. So, further research should focus on the development of an automatic criterion for assessing normalization quality and research of normalization result stability under various distortions: geometric transformation, illumination and degree of compression
