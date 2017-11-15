## [What Uncertainties Do We Need in Bayesian Deep Learning for Computer Vision?](https://arxiv.org/abs/1703.04977)

#### Key words

- bayesian deep learning, aleatoric uncertainty, epistemic uncertainty

#### Key points

- Authors present a Bayesian deep learning framework combining input-dependent aleatoric uncertainty together with epistemic uncertainty
	- Aleatoric uncertainty captures noise inherent in the observations
	- Epistemic uncertainty accounts for uncertainty in the model
- They tested their Bayesian deep model for semantic segmentation and depth regression tasks
- Thanks to the aleatoric uncertainty introduced, their model is robust to noisy data and results in giving new state-of-the-art accuracy for these vision tasks
- Aleatoric uncertainty is directly output by the model and is learnt implicitly from the loss function
- Epistemic uncertainty is computed by Monte Carlo dropout approach, i.e., by averaging the outputs of the model with different dropout masks
- Aleatoric uncertainty is important for:
	- Large data situations (where epistemic uncertainty is explained away)
	- Real-time applications (aleatoric uncertainty can be computed without expensive Monte
Carlo samples)
- Epistemic uncertainty is important for:
	- Small datasets (where the training data is sparse)
	- Safety-critical applications (because epistemic uncertainty is required to understand examples which are different from training data)

#### Thoughts
