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