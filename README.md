# Image Segmentation
## Problem Statment
We intend to perform image segmentation. **Image segmentation** means that we can group similar pixels 
together and give these grouped pixels the same label. The grouping problem is a **clustering** problem. 
We want to study the use of **K-means** on the Berkeley Segmentation Benchmark.
## Objectives
### Download the Dataset and Understand the Format
- We will use Berkeley Segmentation Benchmark
- The data is available at the following link. http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/BSR/BSR_bsds500.tgz.
- The dataset has 500 images. The test set is 200 images only. We will report our results on the first 50 images of the test set only.
- Visualize the image and the ground truth segmentation
### Segmentation using K-means
Every image pixel is a feature vector of 3-dimension {R, G, B}. We will use this feature representation to do the segmentation.
- We will change the K of the K-means algorithm between {3,5,7,9,11} clusters. 
  - We will produce different segmentations and save them as colored images. 
  - Every color represents a certain group (cluster) of pixels.
- We will evaluate the result segmentation using F-measure, Conditional Entropy for image I with M available ground-truth segmentations. 
  - For a clustering of K-clusters we will report our measures M times and the average of the M trials as well. 
  - Report average per dataset as well.
- Display good results and bad results for every configuration in a, b.
### Big Picture
- Select a set of five images and display their corresponding ground truth against your segmentation results using K-means at K=5.
- Select the same five images and display their corresponding ground truth against your segmentation results using Normalized-cut for the 5-NN graph, at K=5.
- Select the same five images and contrast our segmentation results using Normalized-cut for the 5-NN graph, at K=5 versus using K-means at K=5.
### Tuning
In the previous parts, we used the color features RGB. We did not encode the layout of the pixels. We want to modify that for K-means clustering to 
encode the spatial layout of the pixels.
- Modify the feature vector to include spatial layout.
- Contrast the results obtained by considering the spatial layout vs without.
