# Automated Machine Learning

## AutoML Procedure and Taxonomy

<div style="text-align: center">
<img src="figures/procedure.jpg" width="600px" atl="procedure" caption="Figure credit:"/>
</div>

- Training Data Preparation

## Summary

* [Survey](#survey)
* [Hyperparameter Optimization](#hyperparameter-optimization)
* [Neural Architecture Search](#neural-architecture-search)
* [Automated Feature Extraction](#automated-feature-extraction)
* [Meta Learning](#meta-learning)
* [Transfer Learning](#transfer-learning)
* [Automatic Differentiation](#automatic-differentiation)

## Papers

### Survey

* [Automated Machine Learning: Methods, Systems, Challenges](https://www.automl.org/book/), F. Hutter et al., 2019.
* [Survey on Automated Machine Learning](https://arxiv.org/abs/1904.12054), M-A. Zöller and M. Huber, 2019.

### Hyperparameter Optimization

* **`Hyperband`** [Hyperband: A Novel Bandit-Based Approach to Hyperparameter Optimization](https://arxiv.org/abs/1603.06560), L. Li et al., 2016. ([video](https://www.youtube.com/watch?v=5Mb_IguFDmQ), [demo](https://people.eecs.berkeley.edu/~kjamieson/hyperband.html))
	- This paper treats the hyper-parameter tuning problem as a non-stochastic infinitely many-armed bandit problem. It consists of several brackets that contains different number of configurations, and uses Sequential Halving as subroutine in each bracket with the same budget.
	- An important concept introduced in this paper is "partial training", which means we do adaptive evaluation instead of adaptive selection as state-of-the-art methods.
* **`FABOLAS`** [Fast Bayesian Optimization of Machine Learning Hyperparameters on Large Datasets](https://arxiv.org/abs/1605.07079), A. Klein et al., 2017.
	- The idea is to do partial training by leveraging the subset proportion s as an additional parameter in the optimization.
	- Both the target function and the computational cost are modeled as GPs with a modified Matern kernel and modified Entropy Search acquisition function.
	- The kernel is 5/2 Matern kernel multiplied by a finite-rank covariance function of s.
	- The acquisition function is 1/(c(x,s)+overhead) x ES, which is similar to multi-task ES proposed by Swersky et al. (2013).
* **`BOHB`** [BOHB: Robust and Efficient Hyperparameter Optimization at Scale](https://arxiv.org/abs/1807.01774), S. Falkner et al., 2018.
	- Bayesian optimization (in particular, TPE) combined with Hyperband.
* **`ASHA`** [Massively Parallel Hyperparameter Tuning](https://arxiv.org/abs/1810.05934), L. Li et al., 2018.
	- ASHA is asynchronous Sequential Halving where one configuration is promoted to the next rung if it does not attain its maximum resource and is among the top 1/eta fraction. If no such configuration exists, then a new configuration is added to the base rung.
	- In addition, this paper argued that in the sequential setting, Hyperband by rung can outperform FABOLAS using subset as resource.

### Neural Architecture Search

* [Towards Automated Deep Learning: Efficient Joint Neural Architecture and Hyperparameter Search](https://arxiv.org/abs/1807.06906), A. Zela et al., 2018.
	- This workshop paper casts the NAS problem as a HPO problem, and applied BOHB.

### Automated Feature Extraction

### Meta Learning

* [Bilevel Programming for Hyperparameter Optimization and Meta-Learning](https://arxiv.org/abs/1806.04910), L. Franceschi et al., 2018.
	- This paper proposed an unified view of HPO and metal learning with bilevel programming.
	- The main contribution is an approximate form of the bilevel programming and has been proved to converge to the real problem under some (regularity) assumptions.
	- The experiments are more specific to meta learning though, and don't have much to do with HPO. Gradient-based algorithms like Adam can be used to optimize the hyperparameter vector lambda.

### Transfer Learning

### Automatic Differentiation

