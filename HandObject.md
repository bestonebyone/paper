1. Variational Object-aware 3D Hand Pose from a Single RGB Image
	- Publication: RA-L 2019
	- Input: RGB
	- Hand model: Keypoint
	- Assumption: For grasping similar  objects, the grasping poses(i.e. canonical pose) are similar.
	- Contribution: Metric learning for similar objects
	- Weaknesses or Comments:

2. H+O: Unified Egocentric Recognition of 3D Hand-Object Poses and Interactions(CVPR 2019)
	- Publication: CVPR 2019
	- Input: RGBSequences
	- Hand model: Keypoint
	- Assumption: All the groundtruth of hand poses, object poses, object and action are given.
	- Contribution: Jointly estimates the 3D hand and6D object poses, and recognizes the object and action classes
	- Weaknesses or Comments:

3. Learning joint reconstruction of hands and manipulated objects
	- Publication: CVPR 2019 
	- Input: RGB
	- Hand model: Mano Mesh
	- Assumption: ShapeNet dataset is used for Object mesh reconstrucion
	- Contribution: Mano (hand mesh) + object mesh (fromShapeNet) +contact  loss(Attraction loss + Repulsion loss)
	- Weaknesses or Comments:

4. Resolving 3D Human Pose Ambiguities with 3D Scene Constraints
	- Publication: ICCV 2019
	- Input: RGB or RGBD
	- Body model: SMPLify-X mesh
	- Assumption: Static 3D scene(signed distance field) is given(scanning the scene in advance)
	- Contribution:
		- address the body interacting with 3D scene  
		- SMPLify-X +Penetration Term
	- Weaknesses or Comments:

5. InteractionFusion: Real-time Reconstruction of Hand Poses and Deformable  Objects in Hand-object Interactions
	- Publication: SIGGRAPH 2019
	- Input: Two Depth Sequences
	- Hand model: sphere mesh
	- Assumption: non-rigidity majorly happens around contact points
	- Contribution: 
		- Hand-Object Segmentation 
		- nonrigid objects 
		- Energy Term for Hand Tracking, Object(additional object deformation term) and Contact Constraint 
	- Weaknesses or Comments:

6. Joint 3D tracking of a deformable  object in interaction with a hand
	- Publication: ECCV 2018
	- Input: RGBD sequence
	- Hand model: Mesh
	- Assumption: 
		- For the first frame, the mesh template is manually registered to the visual data
		- only fingertips can contact object 
	- Contribution: deformable object + Hand-object contact constraint
	- Weaknesses or Comments:

7. Robust Hand Pose Estimation during the Interaction with an Unknown Object
	- Publication: ICCV 2017
	- Input: Depth
	- Hand model: Keypoint
	- Assumption: 
		- the shape of an object causes a configuration of the hand in the form of a hand grasp
		- pretrain object model
		- global orientation + grasp type = hand pose 
	- Contribution: Use of object shape information as a latent cue to estimate a hand pose in the form of grasp classification
	- Weaknesses or Comments:

8. Back to RGB: 3D tracking of hands and hand-object interactions based on short-baseline stereo
	- Publication: ICCV 2017 workshop
	- Input: RGB stereo sequence
	- Hand model: Mesh
	- Assumption: hand and object model are given 
	- Contribution: stereo RGB input
	- Weaknesses or Comments:

9. Real-time Joint Tracking of a Hand Manipulating an Object from RGB-D Input
	- Publication: ECCV 2016
	- Input: RGBDsequence
	- Hand model: spheres model
	- Assumption: spheres models for hand and object
	- Contribution: 
		- 3D articulated Gaussian mixture alignment (spheres models) for hand and object 
		- torch constraints
	- Weaknesses or Comments:

10. Articulated Distance Fields for Ultra-Fast Tracking of Hands Interacting
	- Publication: SIGGRAPH Asia 2017
	- Input: depth sequence
	- Hand model: signed distance field
	- Assumption: 
	- Contribution: show how to volumetrically deform a single dense signed distance field (SDF) using a skinned tetrahedral mesh
	- Weaknesses or Comments: