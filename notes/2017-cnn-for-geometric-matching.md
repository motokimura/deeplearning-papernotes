## [Convolutional Neural Network Architecture for Geometric Matching](https://arxiv.org/abs/1703.05593)

#### Key words

- end-to-end trainable geometry/image matching

#### Key points

- Main contributions:
	- Propose a CNN architecture for geometric matching, which is based on three main components that mimic the standard steps of feature extraction, matching and model parameter estimation, while being trainable end-to-end
	- Demonstrate that the network can be trained from synthetically generated imagery without the need for manual annotation and that the matching layer significantly increases generalization capabilities to never seen before images
	- The same model can perform both instance-level and category-level matching giving state-of-the-art results on the challenging Proposal Flow dataset

- Methods:
	- Dense feature extraction with pretrained VGG16 network 
	- Mathing based on the extracted feaure similarities computed by correlation layer
	- Model parameter estimation with some convolution layers following the correlation layer

#### Thoughts

- Possible applications:
	- Satellite image registration (image to image, or image to vector map)
	- Vehicle or robot localization with raster or vector maps
