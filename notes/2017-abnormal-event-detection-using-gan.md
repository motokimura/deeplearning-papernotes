## [Abnormal Event Detection in Videos using Generative Adversarial Nets](https://arxiv.org/abs/1708.09644)

#### Key words

- anomaly detection, generative adversarial networks, video analysis

#### Key points

- Authors introduced a generative deep learning based mathod on two conditional GANs for abnormal event detection in video frames of crowded scene
- Challenges of the abnormal event detection
	- Few dataset for abnormal events
	- Definition of abnormal event is not easy
- Methods
	- Train 2 conditional GANs below only with the normal frames and corresponding optical-flow images
		- GAN which generates the optical-flow image from a single video framme
		- GAN which generates the single video frame from an optical-flow image
	- At testing time, as the abnormal frames are not inclued in the training data, the GANs cannot reconstruct the abnormal regions so they can be detected by computing local differences between the real and generated data
	- Local difference computation
		- For video frame local difference, semantic difference is computed using pre-trained AlexNet
		- For optical-flow local difference, simple pixel-bi-pixel difference is computed
	- Weighted sum of the 2 difference images represents the output heatmap for the abnormal events

#### Thoughts