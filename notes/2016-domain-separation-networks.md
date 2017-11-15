## [Domain Separation Networks](https://arxiv.org/abs/1608.06019)

#### Key words

- domain adaptation

#### Key points

- Most of previous approaches focus only on creating a mapping or shared representation between the two domains, they ignore the individual characteristics of each domain
- In contrast,authors propose a model which can explicitly learn to extract image representations that are partitioned into two subspaces: 
	- One component which is private to each domain 
	- The other which is shared across domains
- Architecture of the model is shown in Fig.1
- Loss for the training is the summation of 4 loss terms
	- "Task" term : task specific loss, e.g., cross entropy for classification task (computed only for the labeled dataset, i.e., ones from the source domain)
	- "Reconstruction" term : distance between the model input and domain-shared decoder output
	- "Difference" term : orthogonality between the features encoded by the domain-shared and domain-private encoders
	- "Similarity" term : distance between the features encoded by the domain-private encoders
- "Difference" and "similarity" loss are important for the model to learn domain-specific and domain-shared image representations separately, accordingly

#### Thoughts

- The model may be useful to analyze the aerial or satellite imageries taken by different sensors but at the same target region
- How the optimal values for the weight parameters for 4 loss terms (hyper parameters) can be found?
