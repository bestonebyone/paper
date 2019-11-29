MANO is learned from around 1000 high-resolution 3D scans of hands of 31 subjects in a wide variety of hand poses

1. collect a new database of detailed hand scans of 31 subjects in up to 51 poses

2. use those data to build a statistical hand model

MANO has components:
- a template shape
- kinematic tree
- shape and pose blend shapes
- blend weights
- a joint regressor

The pose space uses linear blend skinning for simplicity, with corrective blend shapes that are automatically learned from the scans.

Consequently we reduce the dimensionality of the pose space by computing a linear embedding of the pose parameters from our dataset.

a skinning function(LBS) W

an articulated rigged body mesh with shape T

a kinematic tree, joint locations J

pose \theta

shape \beta

blend weights W
