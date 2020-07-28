## Other sources
1. [Prior over functions: Gaussian process](https://towardsdatascience.com/prior-over-functions-gaussian-process-1c58e8c40272)

## Bayesian Neural Networks
1. [PoRB-Nets: Poisson Process Radial Basis Function Networks](http://auai.org/uai2020/proceedings/554_main_paper.pdf)
	- Scope:
		1. Data is scarce
		1. Uncertainty must be quantified
	- Related work: 
		1. Gap - Common wright priors encode little functional knowledge. Solution - Bayesian neural networks are flexible function priors (suited to situations where data is scarce and uncertaintly must be quantified).
		1. Gap - Common BNN priors are highly non-stationary.
	- Background:
		1. Bayesian neural networks (BNNs) assume a prior $w, b ~ p(w, b)$.
		1. Radial basis function networks (RBFNs) are classical shallow neural networks that approximate arbitrary nonlinear functions through a linear combination of linear kernels.
	- Contributions:
		1. **Novel prior** over radial basis function (RBF) networks - Allows for independent specification of functional amplitude variance and lengthsale (inverse lengthscale corresponds to concentration of RBFs).
		1. Prove consistency and approximate variance stationarity, when lengthscale is uniform over input space.
		1. Infer input dependence of lengthscale, when unkown.