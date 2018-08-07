# Automatic Machine Learning

## Summary

* [Hyperparameter Optimization](#hyperparameter-optimization)
* [Model Search](#model-search)
* [Meta Learning](#meta-learning)
* [Transfer Learning](#transfer-learning)

## Papers

### Hyperparameter Optimization

* **`Hyperband`** [Hyperband: A Novel Bandit-Based Approach to Hyperparameter Optimization](https://arxiv.org/abs/1603.06560), L. Li et al., 2016. ([video](https://www.youtube.com/watch?v=5Mb_IguFDmQ), [demo](https://people.eecs.berkeley.edu/~kjamieson/hyperband.html))
	- This paper treats the hyper-parameter tuning problem as a non-stochastic infinitely many-armed bandit problem. It consists of several brackets that contains different number of configurations, and uses Sequential Halving as subroutine in each bracket with the same budget.
* **`BOHB`** [BOHB: Robust and Efficient Hyperparameter Optimization at Scale](https://arxiv.org/abs/1807.01774), S. Falkner et al., 2018.
	- Bayesian optimization (in particular, TPE) combined with Hyperband.

### Model Search

* [Towards Automated Deep Learning: Efficient Joint Neural Architecture and Hyperparameter Search](https://arxiv.org/abs/1807.06906), A. Zela et al., 2018.

### Meta Learning

* [Bilevel Programming for Hyperparameter Optimization and Meta-Learning](https://arxiv.org/abs/1806.04910), L. Franceschi et al., 2018.
	- This paper proposed an unified view of HPO and metal learning with bilevel programming.
	- The main contribution is an approximate form of the bilevel programming and has been proved to converge to the real problem under some (regularity) assumptions.
	- The experiments are more specific to meta learning though, and don't have much to do with HPO. Gradient-based algorithms like Adam can be used to optimize the hyperparameter vector lambda.

### Transfer Learning

