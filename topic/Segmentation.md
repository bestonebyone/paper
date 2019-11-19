1. Depth-aware CNN for RGB-D Segmentation
	- Publication: ECCV2018
	- Input: RGBD
	- Assumption: **pixels with the same semantic label and similar depths should have more impact on each other**
	- Contribution:
		- depth similarity between pixels
		- integrate geometry in depth image with CNN
		- depth-aware convolution and depth-aware average pooling
		- operators can be easily integrated into existing CNNs
	- Weaknesses or Comments:


2. Fully Convolutional Networks for Semantic Segmentation
	- Publication: CVPR2015
	- Input: RGB
	- Assumption:
	- Contribution:
		- propose fully convolutional for Segmentation
		- define a **skip architecture** that combines semantic information from a deep, coarse layer with appearance information from a shallow, fine layer to produce accurate and detailed segmentations
	- Weaknesses or Comments: time-consuming


3. Cascaded Feature Network for Semantic Segmentation of RGB-D Images
	- Publication: ICCV2017
	- Input: RGBD
	- Assumption: To compute the representation of object/scene relationships, consider **receptive field** with respect to the **underlying image structure**
	- Contribution: 
		- a cascaded feature network (CFN) with parallel branches, each of which focuses on semantic segmentation of regions of certain scene-resolution
		- **Context-aware receptive field (CaRF) from depth maps** will provide a better control on the relevant contextual information of the Cascaded features
		- CaRFs are computed based on super-pixels, which are defined by the underlying scene structures
	- Weaknesses or Comments: check super-pixels later


4. 3D-SIS: 3D Semantic Instance Segmentation of RGB-D Scans
	- Publication: CVPR2019
	- Input: multi-view RGBD Scans
	- Assumption: 
	- Contribution: 
		- jointly learn from both geometric and color signal
		- leverages RGB by associating 2D images with the volumetric grid based on the pose alignment of the 3D reconstruction
		- Both 3D geometry and 2D color images are taken as input and used to jointly learn semantic features for 3D object detection and 3D instance segmentation
		- For each image, we first extract 2D features for each pixel with a series of 2D convolutions; we then backproject the resulting feature vector to the associated voxel in the 3D grid.
	- Weaknesses or Comments:


5. OCNet: Object Context Network for Scene Parsing
	- Publication: arXiv
	- Input: RGB
	- Assumption: the label of a pixel is the category of the object that the pixel belongs to
	- Contribution: 
		- inspired by the self-attention approach
		- introduce an object context pooling (OCP) scheme, which represents each pixel by exploiting the set of pixels that belong to the same object category with such a pixel, and we call the set of pixels as object context
		- **compute the similarities between each pixel** and all the pixels, forming a so-called object context map for each pixel served as a surrogate for the true object context
		- represent the pixel by aggregating the features of all the pixels weighted by the similarities
		- feeds the input image, lets the feature map go through an object context module, yields an updated feature map, **predicts the label for each pixel**, up-samples the label map
	- Weaknesses or Comments: check self-attention approach later