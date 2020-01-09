1. Detecting and Recognizing Human-Object Interactions
	- Publication: CVPR 2018
	- Input: RGB
	- Assumption: the **appearance of a person (their pose, clothing, action)** is a powerful cue for localizing the objects they are interacting with
	- Contribution: 
		- address the task of detecting ⟨human, verb, object⟩ triplets
		- a person’s appearance is highly informative for inferring where the target object of the interaction may be located. The search space for the target object can thus be **narrowed by conditioning on this** estimation. Note that there are many possible objects interacting with a detected person.
	- Weaknesses or Comments: 
		- a person can simultaneously take multiple actions and an action may not involve any objects
		- the purpose is similar to H+O: Unified Egocentric Recognition of 3D Hand-Object Poses and Interactions.



2. You2Me: Inferring Body Pose in Egocentric Video via First and Second Person Interactions
	- Egocentric Video
	- body pose
	- camera wearer
	- LSTM
	- https://github.com/BielColl/Human-Motion-Dataset-in-the-Wild-MAT-
	- https://upcommons.upc.edu/bitstream/handle/2117/167741/tfg-report-gabriel-coll-ribes.pdf