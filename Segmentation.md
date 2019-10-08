1. Depth-aware CNN for RGB-D Segmentation
	- Publication: ECCV2018
	- Input: RGBD
	- Assumption: pixels with the same semantic label and similar depths should have more impact on each other
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
		- define a skip architecture that combines semantic information from a deep, coarse layer with appearance information from a shallow, fine layer to produce accurate and detailed segmentations
	- Weaknesses or Comments: time-consuming
