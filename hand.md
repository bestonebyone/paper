 # [Hand Collection](https://xinghaochen.github.io/awesome-hand-pose-estimation/)


## CVPR2019

1. Point-to-Pose Voting based Hand Pose Estimation using Residual Permutation Equivariant Layer

- Permutation Equivariant Layer
- point-to-pose voting
- weighted fusion
- for depth hand

2. H+O: Unified Egocentric Recognition of 3D Hand-Object Poses and Interactions

- jointly estimates the 3D hand and object poses from a single RGB image
- input a sequence of frames and outputs perframe 3D hand and object pose predictions along with the estimates of object and action categories for the entire sequence.
- 3D hand pose estimation + object pose estimation + object recognition + activity classification
- 3D grid
- subdivide image into a grid of HxWxD cells and each cell contains a vector stands for hand and object pose predictions, object and confidence values.

3.  Self-supervised 3D hand pose estimation through training by fitting

- a self-supervised learning framework for depth hand with sphere model and model fitting losses

4.  CrossInfoNet: Multi-Task Information Sharing Based Hand Pose Estimation

- a new pose regression network architecture decomposes hand pose estimation task into palm pose estimation sub-task and finger pose estimation sub-task, and adopts two-branch cross-connection structure to share the information  for depth input

5. Expressive Body Capture: 3D Hands, Face, and Body from a Single Image

- (SMPL-X) use thousands of 3D scans (including body,hand, face) to train a Unified model of the human body, fully articulated hands and an expressive face. 
-  (SMPLify-X) shape parameters trained jointly for the face, hands and body
- regress the parameters of proposed model directly from a single RGB images
- data term loss + a VAE-based body pose prior + collision term +  Gender Classifier

6. Learning joint reconstruction of hands and manipulated objects

- using RGB images as input
- regularize the joint reconstruction of hands and objects with manipulation constraints.
- propose a new large-scale synthetic dataset, ObMan, with hand-object manipulations.
- predicts the hand(MANO) and object(AtlasNet + symmetric Chamfer loss + edge-regularization loss + curvature-regularizing loss) meshes
- manipulation constraints : the repulsion loss penalizes interpenetration while the attraction loss encourages the contact regions to be in contact with the object

7. 3D Hand Shape and Pose Estimation from a Single RGB Image

- propose a Graph CNN based method to reconstruct a full 3D mesh of hand surface
- large-scale synthetic RGB-based 3D hand shape and pose dataset 

8. 3D Hand Shape and Pose from Images in the Wild

- predicts both 3D hand shape and pose from RGB images and optionally 2D joint heat-maps
- use the MANO hand model(3D joint loss + mask loss + Regularization + 2D joint re-projection loss)

9. Pushing the Envelope for RGB-based Dense 3D Hand Pose Estimation via Neural Rendering

- MANO supervised by 2D segmentation masks and 3D skeletons.
- Self-supervised data augmentation : generate pairs of 3D meshes, and the corresponding rendered 2D masks and RGB images(neural texture renderer,find in reference Neural 3D mesh renderer)

10. Monocular Total Capture: Posing Face, Body, and Hands in the Wild

- reconstructs the motion from body, face, and fingers represented by a 3D deformable mesh model from a monocular image or video
- use an efficient representation called 3D Part Orientation Fields (POFs) (why POFs?)
- a new 3D human motion dataset 
- photometric consistency across time

11. Disentangling Latent Hands for Image Synthesis and Pose Estimation

- a disentangled representation based cross-modal vae
- disentangling rgb hand into pose and content

## ECCV 2018

1. HandMap: Robust Hand Pose Estimation via Intermediate Dense Guidance Map Supervision

- hand pose estimation framework via intermediate dense guidance map supervision for depth input
- ResNet module (regression based) + Dense guidance map supervision > Hourglass
- combines detection based method and regression based method, and benefits from the added accuracy of intermediate predictions
- feature space supervision via dense guidance maps

2. HBE: Hand Branch Ensemble network for real time 3D hand pose estimation

- Network: design a novel three-branch( correspond to the three parts of a hand: the thumb, the index finger and the other fingers) Convolutional Neural Networks for depth inputs
- Low-dimensional embedding: Inspired by Deep Prior, the label dimensions (J × 3) of the training data are reduced by PCA and used as the ground truth of the bottleneck embedding layer

3. Weakly-supervised 3D Hand Pose Estimation from Monocular RGB Images

- propose depth regularizer for weakly-supervised learning for RGB-based hand pose estimation

4. Point-to-Point Regression PointNet for 3D Hand Pose Estimation

- a stacked network architecture for PointNet with intermediate supervision for 3D point cloud inputs
- generate heat-maps as well as unit vector fields
- decompose neighboring points of the joints into heat-maps on point cloud and unit vector field on point cloud as groundtruth
- The hand joint location can be inferred from the corresponding offset vectors and 3D points using weighted average

5. Joint 3D tracking of a deformable object in interaction with a hand

- tracking in 3D, the interaction of a hand and a non-rigid object(like Paper folding) undergoing complex deformations from RGBD input
- jointly considers the hand, the deformable object and the hand/object contact points
- several hand/object contact configuration hypotheses
- hand(mesh using blender) + Deformable object model(template mesh)

6. Occlusion-aware Hand Pose Estimation Using Hierarchical Mixture Density Network

- tackle the self-occlusion issue and provide a complete description of observed poses given an input depth image
- hierarchical mixture density networks(HMDN) produces interpretable and diverse candidate samples
- a sphere model generate the visibility labels from the available pose labels

7. Hand Pose Estimation via Latent 2.5D Heatmap Regression

- a hand pose estimation framework via 2.5d representation and soft-argmax for RGB inputs 

## CVPR 2018

1. First-Person Hand Action Benchmark with RGB-D Videos and 3D Hand Pose Annotations

- first dataset to help the study of egocentric dynamic hand-object actions and poses
- use mo-cap system that automatically infers the 3D location of 21 joints of a hand model via 6 magnetic sensors and inverse kinematics.
- evaluate 18 baselines and state-of-the-art approaches

2. Learning Pose Specific Representations by Predicting Different Views

- semi-supervised learning, latent space learning and multiple views learning for depth inputs
- given only the pose and shape parameters of a hand, the hand’s appearance from any viewpoint can be approximated
- The training process of this model reveals an implicit pose representation in the latent space
- explore Adversarial training loss

3. Hand PointNet: 3D Hand Pose Estimation using Point Sets

- take 3D point cloud that models the visible surface of the hand for pose regression
- normalize the 3D point cloud in an oriented bounding box (OBB) to make the network input robust to global hand rotation
- design a fingertip refinement network that directly takes the neighboring points of the estimated fingertip location as input to refine the fingertip location

4. Dense 3D Regression for Hand Pose Estimation

- unit vector field + 3D heat map + 2D heat map
- works on dense pixel-wise estimation(based on hourglass) for depth inputs
- formulate 3D hand pose estimation as a dense regression
- a non-parametric post-processing method aggregating pixel-wise estimates to 3D joint coordinates

5. Cross-modal Deep Variational Hand Pose Estimation

- shared latent space
- cross modal variational autoencoder for RGB inputs and an iterative training strategy

6. Feature Mapping for Learning Fast and Accurate 3D Pose Inference from Synthetic Images

- exploit synthetic images for depth hand
- domain transfer between synthetic and real images can be achieved easily in the case of 3D pose inference
- a network to map features extracted from a real image to the feature space of synthetic images
- The feature mapping network only trains the features from real images, not the features from synthetic images
- mapping network (domain adaptation)

7. GANerated Hands for Real-Time 3D Hand Tracking from Monocular RGB

- for RGB inputs
- Kinematic Hand Model : Joint Angle Constraints + 3D Fitting Term + Temporal Smoothness + 2D Fitting Term
- offline data augmentation via GeoConGAN (Cycle GAN)

8. V2V-PoseNet: Voxel-to-Voxel Prediction Network for Accurate 3D Hand and Human Pose Estimation from a Single Depth Map

- we firstly cast the 3D hand and human pose estimation problem from a single depth map into a voxel-to-voxel prediction that uses a 3D voxelized grid and estimates the per-voxel likelihood for each keypoint. We design our model as a 3D CNN that provides accurate estimates while running in real-time. 
- use 3D voxelized depth map to predict 3D heatmap

9. Augmented skeleton space transfer for depth-based hand pose estimation

- Skeleton augmenta􏰅tion
- synthesize data in the skeleton space
- train a separate hand pose generator which synthesizes the depth map from the skeleton entries
- HPG-HPE combination satisfies the cycle consistency

## ICCV 2017

1. Learning to Estimate 3D Hand Pose from Single RGB Images

- first work to estimate hand pose from RGB
- disentangle 3D hand into viewpoint and canonical hand pose

2. Real-time Hand Tracking under Occlusion from an Egocentric RGB-D Sensor

- hand-object interactions from egocentric viewpoints
- A photorealistic data generation framework. 
- use a merged reality framework to track a real hand, where all joint positions are annotated, interacting with a virtual object
- uses two subsequently applied CNNs to localize the hand and regress 3D joint locations
- EgoDexter dataset + SynthHands dataset

3. Robust Hand Pose Estimation during the Interaction with an Unknown Object

- hand and unknown object interaction from depth inputs
- reconstructed hand mesh model from skeleton estimation
- hand grasp classification(estiamte global orientations of the hand and grasp type ) + a nearest neighbor search from the restricted space 
- To generate a large database of the synthetic human grasps, we simulate 3D hand and CAD models.
- a synthetic dataset that is virtually simulated with 3D mesh models
- reconstructed synthesized images eliminate pixel-wise artifacts (e.g., holes or missing pixels) 
- original images without compression distortion
- fuse the depth images by averaging the input(original) and output(synthesized) images

4. Learning Hand Articulations by Hallucinating Heat Distribution

- for depth
- hallucination network is guided to mimic the intermediate responses of the heat distribution modality from a paired depth image
- take depth features and auxiliary modality features(side information)
- At training time, our modality hallucination network takes as input a depth image and is trained to capture the corresponding heat distribution modality.
- At testing time, just takes depth as input
