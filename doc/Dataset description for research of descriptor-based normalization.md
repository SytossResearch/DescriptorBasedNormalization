<h1>Dataset description for research of descriptor-based normalization</h1>

The SYTOSS_NURE_pngPairs100 dataset was constructed to research the normalization approach based on the analysis of key points. 

<h3>The brief information about the dataset SYTOSS_NURE_pngPairs100</h3>

***Equipment:*** Sony Alpha a6000 camera (raw images in ARW: RawDataset_SYTOSS_NURE_arw )

***Format and size of the images:*** the raw images were converted to PNG (lossless compression) and changed to a size of 600-400 or 400-600 pixels.

***Number of image pairs:*** 100 pairs of photo images

***Dataset content:*** the dataset contains five types of scenes (20 images in each set) (Fig.6a–e):
*	Building – buildings, city;
*	Picture_outside – plane images outside (graffiti, posters and other plane images found at the streets);
*	Picture_inside – plane images inside (for example, interior images, pictures, books);
*	Texture_artificial – artificial textures;
*	Texture_nature – natural textures.

The each pair has geometric transformations of various complexity (displacement, scale, rotation, changes in the viewing angle).

To test the descriptor-based normalization in the most complex lighting transformation, we used the small set Day_Night_pngPairs3, which consists of 3 image pairs with the SYTOSS_NURE_pngPairs100 dataset properties (equipment, size, format, geomantic transformation), but in each pair, one image is shot at day and the other at night (Fig.6f).

<p align="center">
  <img src="/doc/images/dataset2.png" width="400" />
  <br>
  Fig.6. – Image pairs examples for each set from SYTOSS_NURE_pngPairs100 <br>(a – Building; b – Picture_outside; c – Picture_ inside; d – Texture_artificial; e – Texture_nature) and Day_Night_pngPairs3(f)
<p>
<br>
