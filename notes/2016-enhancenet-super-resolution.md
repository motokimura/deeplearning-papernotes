## [EnhanceNet: Single Image Super-Resolution Through Automated Texture Synthesis](https://arxiv.org/abs/1612.07919)

#### Key words

- super resolution, perceptual loss, texture matching loss, adversarial training

#### Key points

- Most of the approaches for single image super resolution use MSE in the image space both for training and evaluation
- If MSE in image space is used for training, the generated HR images probe to blur
- Accordingly, MSE or PSNR are not appropriate to evaluate the generated HR images
- In order to resolve this problem, the authors propose following: 
	- Use combo of GAN loss, perceptual loss, and texture loss for training instead of MSE in image space (perceptual loss and texture loss are the similar with the ones used for deep style transfer)
	- Use the performance of state-of-the-art object recognition models as a metric to evaluate image reconstruction algorithms
- Some minor but important gradients:
	- For up-sampling, nearest neighbor is used instead of deconvolution layers
	- No bicubic interpolation before feeding inputs
	- Residual learning proposed by Kim et. al.

#### Thoughts

- How the optimal values for the weight parameters for different loss terms can be found? (grid search?)
