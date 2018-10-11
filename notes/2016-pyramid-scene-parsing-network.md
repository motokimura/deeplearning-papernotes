## [Pyramid Scene Parsing Network](https://arxiv.org/abs/1612.01105)

#### Key words

- semantic segmentation, scene parsing, pyramid pooling module, PSPNet

#### Key points

- Authors proposed pyramid scene parsing network (PSPNet) with the capability of understanding global context information by different-regionbased context aggregation through pyramid pooling module
- A single PSPNet yields the new record of mIoU accuracy 85.4% on PASCAL VOC 2012 and accuracy 80.2% on Cityscapes
- Methods
	- First use CNN to get the feature map of the last convolutional layer 
	- A pyramid parsing module is applied to harvest different sub-region representations, followed by upsampling and concatenation layers to form the final feature representation, which carries both local and global context information in
	- The representation is fed into a convolution layer to get the final per-pixel prediction
	- As the feature extraction CNN, authors used ResNet and added auxiliary loss to effectively train the network
- PSPNet addressed common issues of misclassification:
	- Mismatched relationship
	- Confusion categories
	- Inconspicuous classes

#### Thoughts
