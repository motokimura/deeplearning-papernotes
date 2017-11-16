## [Fast Dense Feature Extraction with CNNs that have Pooling or Striding Layers](http://av.dfki.de/publications/fast-dense-feature-extraction-with-cnns-that-have-pooling-or-striding-layers/)

#### Key words

- dense feature extraction, multi-pooling

#### Key points

- An approach to compute patch-based local feature descriptors efficiently in presence of pooling and striding layers for whole images at once
- Methods
	- All pooling layers in the feature extractor are replaced with multi-pooling layers
	- Multi-pooling layer contains a set of pooling operations with different shift distances
	- The different pooling outputs inside the multi-pooling layer are stacked in an extra output dimension
	- The outputs by multi-pooling layer are unwarped by corresponding unwarp-pooling layers
	- This unwarp operation can be implemented with solely transpose and reshape operations
- Experiments
	- The execution time barely takes more time for larger input images as far as the memory is enough for the computation

#### Thoughts

- Simple but highly effective and general way for dense feature extraction
- Useful to extract features densely from very large images such as satellite images