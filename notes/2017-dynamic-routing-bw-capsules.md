## [Dynamic Routing Between Capsules](https://arxiv.org/abs/1710.09829)

#### Key words

- capsule, routing-by-agreement, CapsNet

#### Key points

- Key concepts of CapsNet
	- Capsule: a group of neurons whose activity represents the instantiation on the entity
		- Length of its activity represents the probability that the entity exists
		- Orientation of its activity represents the properties of the entity
	- Routing-by-agreement: dynamic routing between capsules
		- A lower-level capsule prefers to send its output to higher level capsules whose activity vectors have a big scalar product with the prediction coming from the lower-level capsule
		- Far more effective than the very primitive form of routing implemented by max-pooling, which allows neurons in one layer to ignore all but the most active feature detector in a local pool in the layer below
	- Affine transformation of the feature
		- Each connection between lower/higher level capsules have affine transformation matrix whose parameters are acquired by training
		- This represents spatial or other relationships between lower/higher level capsule features
		- This enables CapsNet to learn hierarchical relationships between lower/higher level features
- Experiment on MNIST dataset
	- Authors constructed and tested CapsNet with 2 conv layers for MNIST classification task
	- The second conv layer (PrimaryCaps) is a convolutional capsule layer and contains 32x6x6 8D capsules
	- The final layer (DigitCaps) has one 16D capsule per digit class 
	- Each capsule of DigitCaps receives input from all the capsules in the PrimaryCaps with routing-by-agreement
	- CapsNet also has decoder for reconstructing input so that the authors can visualize what kind of representations are acquired in DigitCaps (see Figure 4)
	- CapsNet is moderately robust to small affine transformations of the training data and has achieved 0.25 test error on MNIST despite its shallow architecture and relatively few parameters

#### Thoughts

- [~~For me not clear why the CapsNet can acquire robustness to affine transformations or view-point variations of the dataset~~](https://medium.com/@pechyonkin/understanding-hintons-capsule-networks-part-ii-how-capsules-work-153b6ade9f66)
- Is it possible to make CapsNet which can handle bigger image input or more complex task like semantic segmentation or object detection?
